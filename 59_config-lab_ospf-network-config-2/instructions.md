# Config Lab: OSPF Network Config 2

Configure o OSPF legado (tradicional) (usando comandos network) entre R1, R2 e R3. Como um meio de permitir que você exercite o comando network, este laboratório varia os requisitos para os comandos network em cada roteador.

**Essa é uma adaptação do lab que pode ser encontrado no link:** [CertSkills](https://www.certskills.com/clab522/)

![Topologia Original](./assets/img/original-topology.png)

## Requisitos do Laboratório

As regras específicas para este laboratório, para todos os três roteadores, são:

1. Configure cada roteador com um router-id de x.x.x.x onde x é igual ao número do roteador.
2. Use a área 0 (zero) do OSPF.
3. Use o número 5 como ID de processo (process ID) do OSPF.
4. Além disso, como o comando network pode usar muitas máscaras curinga (wildcard masks) diferentes, use as seguintes regras ao escolher as máscaras curinga a serem usadas em cada roteador:
    - Roteador R1: Cada comando network deve corresponder apenas a redes classful (redes com classe), isto é, corresponder a redes classe A, B e C.
    - Roteador R2: Cada comando network deve corresponder aos endereços IPv4 específicos das interfaces do roteador.
    - Roteador R3: Cada comando network deve corresponder às sub-redes das interfaces do roteador.

> Note que em uma rede real, você provavelmente escolheria um estilo em vez de outro e o usaria em todos os roteadores. Este laboratório usa uma variedade apenas para lhe dar uma variedade de prática.

## Configuração Inicial

![Topologia](./assets/img/pnet-topology.png)

As configurações abaixo mostram o estado inicial de R1, R2 e R3.

R1

```cisco
hostname R1
!
interface GigabitEthernet0/0
 no shutdown
 ip address 172.16.1.1 255.255.255.0
!
interface GigabitEthernet0/1
 no shutdown
 ip address 172.30.1.1 255.255.255.252
!
interface GigabitEthernet0/2
 no shutdown
 ip address 172.30.1.10 255.255.255.252
```

R2

```cisco
hostname R2
!
interface GigabitEthernet0/0
 no shutdown
 ip address 172.16.2.2 255.255.255.0
!
interface GigabitEthernet0/1
 no shutdown
 ip address 172.30.1.5 255.255.255.252
!
interface GigabitEthernet0/2
 no shutdown
 ip address 172.30.1.2 255.255.255.252
```

R3

```cisco
hostname R3
!
interface GigabitEthernet0/0
 no shutdown
 ip address 172.16.3.3 255.255.255.0
!
interface GigabitEthernet0/1
 no shutdown
 ip address 172.30.1.9 255.255.255.252
!
interface GigabitEthernet0/2
 no shutdown
 ip address 172.30.1.6 255.255.255.252
```

## Arquivos

- [Arquivo inicial do laboratório](./assets/lab/config_lab_ospf_network_config_2_inicial.zip)
- [Arquivo do laboratório resolvido](./assets/lab/config_lab_ospf_network_config_2_resolvido.zip)
