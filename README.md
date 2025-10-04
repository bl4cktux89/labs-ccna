# Labs CCNA – Repositório de Prática

Este repositório reúne laboratórios práticos que utilizo para estudar e revisar os tópicos exigidos na certificação Cisco CCNA. A ideia é centralizar materiais de diferentes fontes confiáveis em um único lugar, oferecendo opções variadas para praticar habilidades de switching, routing e serviços de rede.

## Servidor do Discord

Também criei um servidor no discord, para quem quiser participar ou ajudar: [NetworkLabs](https://discord.gg/VTpuvYmp)

## Fontes dos Laboratórios

- **[CertSkills](https://www.certskills.com)**
- **[Packet Tracer Network](https://www.packettracernetwork.com)**
- **[Jeremy's IT Lab](https://www.jeremysitlab.com)**
- **[Workshops do Gustavo Kalau](https://www.youtube.com/@GustavoKalau/playlists)**

Observação: Este repositório organiza e referencia materiais para estudo. Respeite as licenças/termos de uso originais dos autores e cursos.

## Estrutura do Repositório

Cada diretório representa um tema ou laboratório, contendo:

- `instructions.md`: roteiro do laboratório e objetivos.
- `lab-solution.md`: referência de solução.
- `assets/`: imagens de topologia, capturas de tela e arquivos `.zip` com as topologias.

Lista de laboratórios disponíveis:

- `01_basic-switch-configuration/`
- `02_ethernet-lan-switching/`
- `03_basic-switch-setup/`
- `04_configuring-switch-interfaces/`
- `05_vlan-and-vtp-configuration/`
- `06_port-security/`
- `07_lan-switching-troubleshooting/`
- `08_basic-router-setup/`
- `09_static-routes/`
- `10_rip-v2/`
- `11_ip-routing-troubleshooting/`
- `12_configuring-serial-links/`
- `13_hdlc/`
- `14_ppp/`
- `15_frame-relay/`
- `16_config-lab_cli-passwords-1/`
- `17_config-lab_cli-passwords-2/`
- `18_config-lab_enabling-ssh-and-disabling-telnet/`
- `19_config-lab_switch-ip-1/`
- `20_config-lab_login-security-1/`
- `21_config-lab_cli-miscellany-1/`
- `22_config-lab_switch-duplex-and-speed/`
- `23_config-lab_switch-admin-config/`
- `24_config-lab_switch-ip-config/`
- `25_config-lab_cli-exploration-1/`
- `26_config-lab_cli-exploration-2/`
- `27_config-lab_vlan-basics-3/`
- `28_config-lab_data-and-voice-vlan-1/`
- `29_config-lab_data-and-voice-vlan-2/`
- `30_config-lab_trunking-puzzle-1/`
- `31_config-lab_basic-vlans/`
- `32_config-lab_trunking-for-only-some-vlans/`
- `33_config-lab_rstp-config-1/`
- `34_config-lab_rstp-config-2/`
- `35_config-lab_l2-etherchannel-1/`
- `36_config-lab_l2-etherchannel-2/`
- `37_config-lab_big-vlan-and-stp-lab-1/`
- `38_config-lab_telnet-config/`
- `39_config-lab_ssh-config/`
- `40_config-lab_ipv4-addressess-1/`
- `41_config-lab_ipv4-addressess-2/`
- `42_config-lab_ipv4-addressess-3/`
- `43_config-lab_ipv4-addressess-4/`
- `44_config-lab_ipv4-addressess-5/`
- `45_config-lab_ipv4-static-routes-1/`
- `46_config-lab_ipv4-static-routes-2/`
- `47_config-lab_ipv4-static-routes-3/`
- `48_config-lab_roas-basics-1/`
- `49_config-lab_layer3-switching-1/`
- `50_config-lab_layer3-switching-2/`
- `51_config-lab_layer3-switching-with-svis/`
- `52_config-lab_layer3-switching-with-routed-ports/`
- `53_config-lab_l3-etherchannel-1/`
- `54_config-lab_dhcp-relay/`
- `55_config-lab_router-as-dhcp-client/`
- `56_config-lab_ospf-interface-config-1/`
- `57_config-lab_ospf-interface-config-2/`
- `58_config-lab_ospf-network-config-1/`
- `59_config-lab_ospf-network-config-2/`
- `60_config-lab_ospf-multi-area-ospf-1/`
- `61_config-lab_ospf-multi-area-ospf-2/`
- `62_config-lab_ospf-dr-priority/`
- `63_config-lab_ospf-network-type/`
- `64_config-lab_ospf-router-ids/`
- `65_config-lab_ospf-metrics/`
- `66_config-lab_ipv6-eui64-addressing-1/`
- `67_config-lab_ipv6-global-unicast-addressing-1/`
- `68_config-lab_ipv6-static-routes-1/`
- `69_config-lab_ipv6-static-routes-2/`
- `70_config-lab_ipv6-special-addresses-1/`
- `71_config-lab_ipv6-special-addresses-2/`
- `72_config-lab_standard-numbered-acl-1/`
- `73_config-lab_standard-named-acl-1/`
- `74_config-lab_extended-numbered-acl-1/`
- `75_config-lab_extended-named-acl-1/`
- `76_config-lab_basic-port-security-1/`
- `77_config-lab_basic-port-security-2/`
- `78_config-lab_basic-port-security-3/`
- `79_config-lab_basic-port-security-4/`
- `80_config-lab_dhcp-snooping-1/`
- `81_config-lab_dhcp-snooping-2/`
- `82_config-lab_dai-1/`
- `83_config-lab_cdp-lldp-1/`
- `84_config-lab_ntp-client-and-server/`
- `85_config-lab_syslog-1/`
- `86_config-lab_syslog-2/`
- `87_config-lab_syslog-3/`
- `88_config-lab_dynamic-nat-1/`
- `88_config-lab_static-nat-1/`
- `89_config-lab_interface-pat-1/`
- `90_config-lab_pat-with-a-pool-1/`

## Pré-requisitos

- PNETLab ou EVE-NG
- Conhecimentos básicos de CLI Cisco IOS.

## Como Usar

1. Clone o repositório.
2. Escolha um diretório de lab (ex.: `03_basic-switch-setup/`).
3. Leia o `instructions.md` para entender objetivos e passos.
4. Abra a topologia correspondente na ferramenta (geralmente arquivos em `assets/lab/` → `.zip` contendo `.unl`).
5. Execute as configurações conforme o roteiro.
6. Compare seu resultado com o `lab-solution.md` e ajuste o que for necessário.

Exemplo de clonagem:

```bash
git clone https://github.com/bl4cktux89/labs-ccna.git
cd labs-ccna
```

## Boas Práticas de Estudo

- **Refaça**
- **Varie**
- **Documente**
- **Cronometre**

## Roadmap (ideias futuras)

- Adicionar mais labs de roteamento dinâmico (OSPF, EIGRP básico).
- Adicionar labs de NAT, DHCP, ACLs e serviços.
- Incluir checklists de verificação (show commands) por tópico.

## Contribuição

Sugestões e correções são bem-vindas. Abra uma Issue ou envie um Pull Request com:

- Descrição clara do problema/melhoria.
- Prints/topologias se aplicável.
- Referências (quando derivado de conteúdo de terceiros).

## Licença

Consulte o arquivo `LICENSE` para detalhes. Materiais de terceiros citados/organizados aqui permanecem sob suas respectivas licenças.
