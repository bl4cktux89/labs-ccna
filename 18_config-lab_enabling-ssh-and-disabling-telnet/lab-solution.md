# Resolução do Lab Abaixo

## Explicação da Solução

> Antes de iniciar:
É importante dizer que o fabricante recomenda a utilização do SSH na versão 2, para satisfazer essa condição, deverá ser gerada uma chave de criptografia com, pelo menos, 768 bits!

### Passo 1: Efetuar o login no SW1

Ao clicar no switch, você receberá o seguinte prompt, seguir com as senhas configuradas previamente e estão nas [instruções](./instructions.md):

```cisco
User Access Verification

Password: certskills
SW1>enable
Password: certskills
SW1#
```

### Passo 2: Configurar a chave SSH para acesso remoto

Agora vamos gerar a chave de criptografia, você vai precisar acessar o modo de configuração global:

```cisco
configure terminal
ip domain-name example.com
crypto key generate rsa
```

A seguir irá aparecer o seguinte prompt, lembre-se de configurar a chave com pelo menos 768 bits para habilitarmos o SSH na versão 2.

```cisco
The name for the keys will be: SW1.example.com
Choose the size of the key modulus in the range of 360 to 4096 for your
  General Purpose Keys. Choosing a key modulus greater than 512 may take
  a few minutes.

How many bits in the modulus [512]: 1024
% Generating 1024 bit RSA keys, keys will be non-exportable...
[OK] (elapsed time was 0 seconds)

SW1(config)#
*Oct  4 20:07:19.892: %SSH-5-ENABLED: SSH 1.99 has been enabled
```

Após gerar a chave, configurar o SSH na versão 2:

```cisco
ip ssh version 2
```

Para garantir que a versão 2 foi habilitada, execute o comando abaixo no modo privilegiado:

```cisco
show ip ssh
```

Se tudo estiver correto, você receberá o prompt a seguir no seu terminal:

```cisco
SSH Enabled - version 2.0
Authentication methods:publickey,keyboard-interactive,password
Encryption Algorithms:aes128-ctr,aes192-ctr,aes256-ctr,aes128-cbc,3des-cbc,aes192-cbc,aes256-cbc
MAC Algorithms:hmac-sha1,hmac-sha1-96
Authentication timeout: 120 secs; Authentication retries: 3
Minimum expected Diffie Hellman key size : 1024 bits
IOS Keys in SECSH format(ssh-rsa, base64 encoded): SW1.example.com
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAAAgQCSIc1pkQIwnKq7HO85svggvD6iFd4wL0SX6s5F/e/O
b4Xm+66f9Kp+B1UX60xIhFSefz3XkW78xR3BfhRXP2Z0MZaGZJBQrSI80rfI+acR17+UxVfR9CIkh5SN
/max8AqhNb+u0XBUS5t5stwDcHzMVeJrO/ZBLOrJOIcDnO5AZQ==
```

> Importante dizer que a saída pode variar, o ponto de atenção deve ser a versão do protocolo, ok?
Observe que acima está escrito **SSH Enabled - version 2.0**

### Passo 3: Criar usuário e senha conforme as regras do lab

Antes de começarmos, gostaria de informar que pode ser que exista uma limitação da imagem utilizada, preciso me informar melhor (sorry guys :(), porque conforme os prompts abaixo, porque não é possível escolher o tipo de criptografia ao criar a senha do usuário:

```cisco
SWT1(config)#username Barney secret 9 Rubble
ERROR: The secret you entered is not a valid encrypted secret.
To enter an UNENCRYPTED secret, do not specify type 9 encryption.
When you properly enter an UNENCRYPTED secret, it will be encrypted.

Please set a password for username

SWT1(config)#username Barney secret 8 Rubble
ERROR: The secret you entered is not a valid encrypted secret.
To enter an UNENCRYPTED secret, do not specify type 8 encryption.
When you properly enter an UNENCRYPTED secret, it will be encrypted.

Please set a password for username

SWT1(config)#username Barney secret 5 Rubble
ERROR: The secret you entered is not a valid encrypted secret.
To enter an UNENCRYPTED secret, do not specify type 5 encryption.
When you properly enter an UNENCRYPTED secret, it will be encrypted.

Please set a password for username
```

Agora vamos criar o usuário Barney, com a senha Rubble criptografada, acesso o modo de configuração global e aplique o comando abaixo:

```cisco
username Barney secret Rubble
```

### Passo 4: Ajustar a configuração de acesso à console e às lines vty

Na primeira parte, vamos ajustar o acesso à console, temos que apagar as configurações anteriores senão as novas não irão funcionar:

```cisco
line console 0
no password
no login
login local
exit
```

Agora vamos ajustar o acesso às lines vty, temos que fazer o mesmo processo que realizamos ao ajustar as configurações da console:

```cisco
line vty 0 4
no password
no login
login local
transport input ssh
```

**Detalhe importante:** se atentar para não esquecer o comando *transport input ssh*

## Verificação

Para garantir que as configurações foram aplicadas corretamente, você pode verificar a configuração atual do equipamento:

```cisco
show running-config
```

Você deve se atentar nos pontos abaixo:

```cisco
ip domain-name example.com
!
interface Vlan1
 ip address 10.1.1.20 255.255.255.0
!
ip route 0.0.0.0 0.0.0.0 10.1.1.1
ip ssh version 2
!
line con 0
 logging synchronous
 login local
line aux 0
line vty 0 4
 login local
 transport input ssh
!
```

Para validar a funcionalidade do SSH, acesse o roteador R1 e faça o teste da conexão:

```cisco
ssh 10.1.1.20
% No user specified nor available for SSH client
```

Observe que se você não informar o usuário, o comando não irá funcionar, execute o comando conforme abaixo:

```cisco
ssh -l Barney 10.1.1.20
Password: Rubble
```

Se a senha inserida for a correta, você entrará no modo usuário (não alteramos os privilégios do usuário):

```cisco
SW1>
```

Se quiser acessar ou aplicar alguma configuração, você pode acessar o modo privilegiado:

```cisco
SW1>enable
Password: certskills
SW1#
```

Aqui chegamos ao final da nossa prática, caso tenha algum comentário ou sugestão, entre em contato:

- [Discord](https://discord.gg/VTpuvYmp)
- [X/Twitter](https://x.com/bl4cktux89)
