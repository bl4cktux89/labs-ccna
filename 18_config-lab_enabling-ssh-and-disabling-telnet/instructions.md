# Config Lab: Enabling SSH and Disabling Telnet

## Requisitos do Laboratório

No blog do Wendell Odom, autor dos guias oficiais do CCNA, os labs foram criados com o Packet Tracer e o CML, aproveitando o embalo, segue o link para o lab original:

- [Config Lab: Enabling SSH and Disabling Telnet](https://www.certskills.com/clab103/)

Você irá configurar um switch Cisco para suportar SSH e não suportar Telnet. Da perspectiva do usuário, uma tentativa de conexão via Telnet deve ser rejeitada para que o usuário nunca veja uma solicitação de senha ou nome de usuário. Os usuários de SSH devem ter o acesso permitido se fornecerem um nome de usuário e senha corretos. Para este laboratório, o switch já foi configurado para suportar IP e com senhas simples; sua tarefa é atualizar a configuração para suportar apenas SSH para usuários remotos.

As regras específicas para este laboratório são as seguintes:

Configure o SSH para usar uma chave de criptografia.
Crie a chave SSH de forma que ela utilize o nome de domínio example.com como entrada.
Crie um par de nome de usuário/senha de Barney/Rubble com a melhor criptografia possível para a senha.
Habilite o suporte para SSH, e apenas SSH, usando os nomes de usuário/senhas criados localmente.

**Topologia Original**
![Topologia Original](./assets/img/00-topology.png)

**Topologia EVE/PNETLAB**
![Topologia EVE/PNETLAB](./assets/img/01-topology.png)

Configuração Inicial

Este laboratório começa com um switch que foi configurado para permitir tanto Telnet quanto SSH no switch, ambos usando um endereço IP simples. O endereço IP de gerenciamento e as senhas de acesso à CLI para o modo de usuário e modo privilegiado (enable) já foram definidos. O Exemplo 1 mostra essa configuração.

### Configuração Inicial

Abaixo, podemos observar a configuração aplicada ao switch SW1 antes do início do seu trabalho neste laboratório. Basicamente, o switch já foi configurado com um endereço IP e um gateway padrão para permitir o acesso via telnet.

```cisco
 hostname SW1
ip route 0.0.0.0 0.0.0.0 10.1.1.1
!
interface vlan1
 ip address 10.1.1.20 255.255.255.0
 no shutdown
!
line vty 0 4
 password certskills
 login
```

### Configuração do Lab CLI Passwords 1

Para responder, basta pensar sobre o laboratório. Consulte seu material de estudo principal para o CCNA, suas anotações, e aplique a configuração no [arquivo inicial do lab](./assets/lab/18_enabling-ssh-and-disabling-telnet_inicial.zip). Depois, confira sua resposta com as [instruções para a solução do lab](./lab-solution.md) e o [lab solucionado](./assets/lab/18_enabling-ssh-and-disabling-telnet_resolvido).

| Device | IP Address|
| --- | --- |
| PC | 10.1.1.11 |
| SRV | 10.1.1.22 |
