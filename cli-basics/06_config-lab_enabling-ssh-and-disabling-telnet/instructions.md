# Config Lab: CLI Exploration

## Requisitos do Laboratório

Você configurará um switch Cisco para suportar SSH e não suportar Telnet. Do ponto de vista do usuário, uma tentativa de conexão via Telnet deve ser rejeitada para que o usuário nunca veja uma solicitação de senha ou nome de usuário. Usuários SSH devem ter o acesso permitido se fornecerem um nome de usuário e senha corretos. Para este laboratório, o switch já foi configurado para suportar IP e com senhas simples; seu trabalho é atualizar a configuração para suportar apenas SSH para usuários remotos.

As regras específicas para este laboratório são as seguintes:

1. Configure o SSH para usar uma chave de criptografia.
2. Crie a chave SSH de forma que ela utilize o nome de domínio 'example.com' como entrada.
3. Crie um par de nome de usuário/senha Barney/Rubble com a melhor criptografia possível para a senha.
4. Habilite o suporte para SSH, e apenas SSH, usando os nomes de usuário/senhas criados localmente.

**Topologia Original**
![Topologia Original](./assets/img/00-topology.png)

**Topologia EVE/PNETLAB**
![Topologia EVE/PNETLAB](./assets/img/01-topology.png)

## Configuração Inicial

Este laboratório começa com um switch que foi configurado para permitir conexões Telnet e SSH, ambas usando um endereço IP simples. O endereço IP de gerenciamento e as senhas de acesso à CLI para o modo de usuário e modo privilegiado (enable) já foram definidos. Abaixo podemos observar essa configuração:

```cisco
 hostname SW1
 enable secret 5 certskills
 ip route 0.0.0.0 0.0.0.0 10.1.1.1
!
interface Ethernet0/0
 switchport trunk allowed vlan 1
 switchport trunk encapsulation dot1q
 switchport mode trunk
!
interface vlan1
 ip address 10.1.1.20 255.255.255.0
 no shutdown
!
line con 0
 password certskills
 logging synchronous
 login
line aux 0
line vty 0 4
 password certskills
 login
```

## Configuração do Lab

Para responder, basta pensar sobre o laboratório. Consulte seu material de estudo principal para o CCNA, suas anotações, e aplique a configuração no [arquivo inicial do lab](./assets/lab/18_config_lab_enabling_ssh_and_disabling_telnet_inicial.zip). Depois, confira sua resposta com as [instruções para a solução do lab](./lab-solution.md) e o [lab solucionado](./assets/lab/18_config_lab_enabling_ssh_and_disabling_telnet_resolvido).

| Device | IP Address|
| --- | --- |
| PC | 10.1.1.11 |
| SRV | 10.1.1.22 |

Aqui chegamos ao final das instruções, caso tenha algum comentário ou sugestão, entre em contato:

- [Discord](https://discord.gg/VTpuvYmp)
- [X/Twitter](https://x.com/bl4cktux89)
