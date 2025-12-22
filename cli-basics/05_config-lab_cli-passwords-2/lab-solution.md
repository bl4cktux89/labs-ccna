# Respostas do Lab Abaixo

Passo 1: Acesso o switch SW1 e aplique as seguintes configurações:

```cisco
enable
configure terminal

username allison password hope
username danielle password love
username tyler password faith

line console 0
login local

line vty 0 4
login local
```

Passo 2: Para validar as configurações, acesse o R1 e aplique os seguintes comandos:

```cisco
telnet 10.1.1.20 /source-interface loopback 0
```

Passo 3: Se você aplicou as configurações corretamente, vai aparecer o prompt abaixo:

```cisco
Trying 10.1.1.20 ... Open


User Access Verification

Username:
```

Passo 4: Insira o nome do usuário, clique em ENTER, insira a senha criada e clique em ENTER novamente, conforme o exemplo abaixo:

```cisco
Username: allison
Password: hope
```

> Ao digitar a senha, se atente, pois o terminal permanece estático!

Passo 5: Efetue o logout:

```cisco
exit
```

Vai aparecer o prompt abaixo:

```cisco
[Connection to 10.1.1.20 closed by foreign host]
```

Passo 6: Repita o Passo 4 até ter testado todos os usuários criados.
