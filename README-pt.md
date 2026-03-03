# Beacon Skill

[![Bounty](https://img.shields.io/badge/bounty-RTC-green)](https://github.com/Scottcjn/rustchain-bounties)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Contributors](https://img.shields.io/github/contributors/Scottcjn/beacon-skill)](https://github.com/Scottcjn/beacon-skill/graphs/contributors)

> **Beacon** é um protocolo de heartbeat e coordenação de agentes de IA. Permite que os agentes mantenham presença, compartilhem status e coordenem atividades através de mensagens de heartbeat periódicas com validação opcional de tokens RTC.

## 🚀 Recursos

- **Protocolo Heartbeat**: Pings leves de agente para agente
- **Broadcast UDP**: Descoberta eficiente de rede local
- **Integração RTC**: Validação opcional de tokens cripto
- **Suporte Multi-Agente**: Coordenar enxames e equipes
- **Saída JSON**: Status e métricas legíveis por máquina
- **Multiplataforma**: Funciona em macOS, Linux e Windows

## 📦 Instalação

### Homebrew (macOS)

```bash
brew tap Scottcjn/homebrew-tap
brew install beacon
```

### Linux

```bash
wget https://github.com/Scottcjn/beacon-skill/releases/latest/download/beacon-linux-amd64
chmod +x beacon-linux-amd64
sudo mv beacon-linux-amd64 /usr/local/bin/beacon
```

### Do Código-Fonte

```bash
git clone https://github.com/Scottcjn/beacon-skill.git
cd beacon-skill
cargo build --release
```

## 💡 Uso

### Iniciar Agente

```bash
# Início básico
beacon start

# Com carteira
beacon start --wallet your-wallet-address

# Modo ouvinte
beacon start --listen-only
```

### Enviar Heartbeat

```bash
# Ping simples
beacon ping

# Com mensagem
beacon ping --message "Trabalhando na documentação"

# Saída JSON
beacon ping --json
```

### Verificar Status

```bash
# Status local
beacon status

# Formato JSON
beacon status --json

# Agente específico
beacon status --agent agent-id
```

## 📖 Documentação

- [Tutorial de Início](TUTORIALS/getting-started.md)
- [Referência da API](docs/API.md)
- [Guia de Configuração](docs/CONFIGURATION.md)
- [Exemplos de Integração](docs/INTEGRATION.md)

## 🤝 Contribuindo

Contribuições são bem-vindas! Veja nosso [Guia de Contribuição](CONTRIBUTING.md) para detalhes.

### Início Rápido

1. Faça fork do repositório
2. Crie um branch de recurso: `git checkout -b feature/my-feature`
3. Faça suas alterações
4. Execute testes: `cargo test`
5. Envie um PR

## 📜 Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

## 🏆 Bounties

Este projeto participa do programa de bounties da RustChain:

- **Documentação**: 2-5 RTC por melhoria
- **Recursos**: 5-20 RTC por recurso
- **Correções de Bugs**: 3-10 RTC por correção

Reivindique bounties com carteira: `joshualover-dev`

Veja [rustchain-bounties](https://github.com/Scottcjn/rustchain-bounties) para oportunidades disponíveis.

## 🔗 Links

- [RustChain](https://github.com/Scottcjn/Rustchain)
- [Programa de Bounties](https://github.com/Scottcjn/rustchain-bounties)
- [Comunidade Discord](https://discord.gg/rustchain)

---

**Construído com ❤️ pela Equipe RustChain**
