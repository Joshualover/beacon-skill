# Beacon Skill

[![Bounty](https://img.shields.io/badge/bounty-RTC-green)](https://github.com/Scottcjn/rustchain-bounties)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Contributors](https://img.shields.io/github/contributors/Scottcjn/beacon-skill)](https://github.com/Scottcjn/beacon-skill/graphs/contributors)

> **Beacon** est un protocole de heartbeat et de coordination pour agents IA. Il permet aux agents de maintenir une présence, partager leur statut et coordonner leurs activités via des messages de heartbeat périodiques avec validation optionnelle de tokens RTC.

## 🚀 Fonctionnalités

- **Protocole Heartbeat**: Pings légers entre agents
- **Broadcast UDP**: Découverte efficace du réseau local
- **Intégration RTC**: Validation optionnelle de tokens crypto
- **Support Multi-Agent**: Coordonner essaims et équipes
- **Sortie JSON**: Statut et métriques lisibles par machine
- **Multi-plateforme**: Fonctionne sur macOS, Linux et Windows

## 📦 Installation

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

### Depuis les Sources

```bash
git clone https://github.com/Scottcjn/beacon-skill.git
cd beacon-skill
cargo build --release
```

## 💡 Utilisation

### Démarrer l'Agent

```bash
# Démarrage basique
beacon start

# Avec portefeuille
beacon start --wallet your-wallet-address

# Mode écoute
beacon start --listen-only
```

### Envoyer Heartbeat

```bash
# Ping simple
beacon ping

# Avec message
beacon ping --message "Travail sur documentation"

# Sortie JSON
beacon ping --json
```

### Vérifier Statut

```bash
# Statut local
beacon status

# Format JSON
beacon status --json

# Agent spécifique
beacon status --agent agent-id
```

## 📖 Documentation

- [Tutoriel de Démarrage](TUTORIALS/getting-started.md)
- [Référence API](docs/API.md)
- [Guide de Configuration](docs/CONFIGURATION.md)
- [Exemples d'Intégration](docs/INTEGRATION.md)

## 🤝 Contribuer

Les contributions sont les bienvenues ! Consultez notre [Guide de Contribution](CONTRIBUTING.md) pour les détails.

### Démarrage Rapide

1. Forkez le dépôt
2. Créez une branche fonctionnelle : `git checkout -b feature/my-feature`
3. Faites vos changements
4. Exécutez les tests : `cargo test`
5. Soumettez une PR

## 📜 Licence

Ce projet est sous licence MIT - voir le fichier [LICENSE](LICENSE) pour les détails.

## 🏆 Bounties

Ce projet participe au programme de bounties RustChain :

- **Documentation**: 2-5 RTC par amélioration
- **Fonctionnalités**: 5-20 RTC par fonctionnalité
- **Corrections de Bugs**: 3-10 RTC par correction

Réclamez les bounties avec le portefeuille : `joshualover-dev`

Voir [rustchain-bounties](https://github.com/Scottcjn/rustchain-bounties) pour les opportunités disponibles.

## 🔗 Liens

- [RustChain](https://github.com/Scottcjn/Rustchain)
- [Programme de Bounties](https://github.com/Scottcjn/rustchain-bounties)
- [Communauté Discord](https://discord.gg/rustchain)

---

**Construit avec ❤️ par l'Équipe RustChain**
