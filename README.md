# Labs CCNA – Repositório de Prática

Este repositório reúne laboratórios práticos que utilizo para estudar e revisar os tópicos exigidos na certificação Cisco CCNA. A ideia é centralizar materiais de diferentes fontes confiáveis em um único lugar, oferecendo opções variadas para praticar habilidades de switching, routing e serviços de rede.

## Fontes dos Laboratórios

- **CertSkills**
- **Packet Tracer Network**
- **Jeremy's IT Lab**
- **Workshops do Gustavo Kalau**

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
- `18_enabling-ssh-and-disabling-telnet/`
- `19_config-lab-switch-ip-1/`
- `20_config-lab-login-security-1/`
- `21_config-lab-cli-miscellany-1/`
- `22_config-lab-switch-duplex-and-speed/`
- `23_config-lab-switch-admin-config/`
- `24_config-lab-switch-ip-config/`
- `25_config-lab-cli-exploration-1/`
- `26_config-lab-cli-exploration-2/`

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
