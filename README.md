# Cybersecurity-journey

> Hands-on cybersecurity journey — networking, Linux, Active Directory, SIEM, detection, incident response and security labs.

## 🎯 Objetivo deste repositório

Registrar, de forma organizada e verificável, cada laboratório, projeto e aprendizado da minha transição de **Suporte Técnico N2 + Desenvolvimento** para **Cibersegurança (Blue Team)** — para consulta própria, acompanhamento de evolução e para qualquer recrutador/gestor técnico que queira ver como eu penso e documento meu trabalho.

## 🗺️ Roadmap

- [x] Setup do ambiente — host 100% Ubuntu, VMs com QEMU/KVM + libvirt (virt-manager)
- [x] Fundamentos de Linux (TryHackMe — Pre Security)
- [x] Fundamentos de redes (TryHackMe — Network Fundamentals, parte gratuita: até o módulo 2, LAN)
- [x] VM descartável com isolamento de rede — QEMU/KVM + nftables ([ephemeral-vm-lab](https://github.com/DevMiranda7/ephemeral-vm-lab))
- [ ] Prática de Linux via OverTheWire Bandit *(em andamento — nível 11/34)*
- [ ] Home Lab de rede: Wireshark + Nmap *(incluindo a captura do tráfego da VM descartável)*
- [ ] Active Directory vulnerável (Windows Server + cliente)
- [ ] SIEM — Wazuh monitorando o ambiente do lab
- [ ] Sysmon + análise de eventos no Windows
- [ ] Projeto "Home SOC" — Wazuh + AD + regras de detecção
- [ ] Certificação CompTIA Security+

## 🔒 Projetos em destaque

### [ephemeral-vm-lab](https://github.com/DevMiranda7/ephemeral-vm-lab) — VM descartável com isolamento de rede

Cada sessão nasce de uma imagem limpa, com hostname, MAC, IP e sub-rede novos, e é destruída por completo ao sair. O disco vive só na RAM.

- **Redes:** bridge e NAT por sessão, DHCP com IP por MAC e regras nftables (cadeias `input` e `forward`) que deixam a VM falar só com a internet pública, bloqueando host, LAN e redes privadas
- **Segurança:** redução de superfície de ataque (sem USB, som e área de transferência), verificação de imagem por GPG e SHA256, chaves SSH efêmeras e AppArmor via `qemu:///system`
- **Validação:** teste de controle do isolamento (o host alcança o roteador, a VM não)
- **Modelo de ameaça:** documentei o que o projeto não resolve (IP público, fingerprint de navegador, escape de VM)

## 🧰 Stack e ferramentas

**Em uso**

`QEMU/KVM` · `libvirt` · `virt-manager` · `nftables` · `cloud-init` · `Ubuntu 24.04 LTS` · `Bash` · `TryHackMe` · `OverTheWire Bandit`

**Planejado (próximas fases)**

`Wireshark` · `Nmap` · `Windows Server/Cliente` · `Kali Linux` · `Wazuh` · `Sysmon` · `PowerShell` · `Python`

## 🧪 Ambiente

- Host: Ubuntu (100% Linux)
- Virtualização: QEMU/KVM com libvirt, gerenciado pelo virt-manager
- VM de estudo: Ubuntu 24.04 LTS (3 vCPUs, 4 GB RAM)
- VMs descartáveis: sessões efêmeras criadas por script (veja o projeto em destaque)

> Sobre o Bandit: seguindo a regra da comunidade OverTheWire, **não publico senhas nem soluções exatas** — apenas conceitos e raciocínio.

## 📌 Status atual

🟡 **Em andamento** — ambiente base configurado, fundamentos de Linux e a parte gratuita de redes concluídos, e o laboratório de VM descartável publicado. Aprofundando na prática com OverTheWire Bandit (nível 11/34); em seguida, Wireshark + Nmap e estudo dirigido para a Security+.

*Atualizado em outubro de 2026, conforme avanço nos estudos. Feedback é bem-vindo.*
