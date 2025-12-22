# Config Lab: OSPF Interface Config 2

Configure o OSPF para a rede do laboratório demonstrada na topologia. No entanto, não utilize a configuração tradicional com comandos network no modo de configuração do OSPF. Em vez disso, use a configuração de interface OSPF.

**Essa é uma adaptação do lab que pode ser encontrado no link:** [CertSkills](https://www.certskills.com/clab520/#1621538143010-3327296b-3256)

![Topologia Original](./assets/img/original-topology.png)

## Requisitos do Laboratório

As regras específicas para este laboratório são:

1. Configure para que cada roteador use um router-id de x.x.x.x onde x é igual ao número do roteador.
2. Não dependa dos endereços IP da interface para a definição dos router-IDs.
3. Use a área 0 (zero) do OSPF.
4. Use o número 50 como process-id (ID de processo) do OSPF.
5. Habilite o OSPF diretamente em cada interface, em vez de usar o método indireto e o comando network do OSPF.

> Assuma que todas as interfaces mostradas no laboratório estão ativas (up) e funcionando.

## Configuração Inicial

![Topologia](./assets/img/pnet-topology.png)

As configurações abaixo mostram o estado inicial de R1 e R2.

R1

```cisco
hostname R1
!
interface ethernet0/1
 no shutdown
 ip address 10.50.100.97 255.255.255.224
!
interface loopback0
 no shutdown
 ip address 1.1.1.1 255.255.255.255
!
interface loopback1
 no shutdown
 ip address 10.50.100.129 255.255.255.224
```

R2

```cisco
hostname R2
!
interface ethernet0/1
 no shutdown
 ip address 10.50.100.98 255.255.255.224
!
interface loopback0
 no shutdown
 ip address 2.2.2.2 255.255.255.255
!
interface loopback1
 no shutdown
 ip address 10.50.101.1 255.255.255.224
 ```

## Arquivos

- [Arquivo inicial do laboratório](./assets/lab/config_lab_ospf_interface_config_2_inicial.zip)
- [Arquivo do laboratório resolvido](./assets/lab/config_lab_ospf_interface_config_2_resolvido.zip)
