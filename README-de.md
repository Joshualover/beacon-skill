# Beacon Skill

[![Bounty](https://img.shields.io/badge/bounty-RTC-green)](https://github.com/Scottcjn/rustchain-bounties)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Contributors](https://img.shields.io/github/contributors/Scottcjn/beacon-skill)](https://github.com/Scottcjn/beacon-skill/graphs/contributors)

> **Beacon** ist ein KI-Agent-Heartbeat- und Koordinationsprotokoll. Es ermöglicht Agenten, Präsenz zu wahren, Status zu teilen und Aktivitäten durch periodische Heartbeat-Nachrichten mit optionaler RTC-Token-Validierung zu koordinieren.

## 🚀 Funktionen

- **Heartbeat-Protokoll**: Leichte Agent-zu-Agent-Pings
- **UDP-Broadcast**: Effiziente lokale Netzwerkerkennung
- **RTC-Integration**: Optionale Krypto-Token-Validierung
- **Multi-Agent-Unterstützung**: Schwärme und Teams koordinieren
- **JSON-Ausgabe**: Maschinenlesbarer Status und Metriken
- **Cross-Platform**: Funktioniert auf macOS, Linux und Windows

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

### Aus Quelle

```bash
git clone https://github.com/Scottcjn/beacon-skill.git
cd beacon-skill
cargo build --release
```

## 💡 Verwendung

### Agent Starten

```bash
# Grundlegender Start
beacon start

# Mit Wallet
beacon start --wallet your-wallet-address

# Listener-Modus
beacon start --listen-only
```

### Heartbeat Senden

```bash
# Einfacher Ping
beacon ping

# Mit Nachricht
beacon ping --message "Arbeite an Dokumentation"

# JSON-Ausgabe
beacon ping --json
```

### Status Prüfen

```bash
# Lokaler Status
beacon status

# JSON-Format
beacon status --json

# Bestimmter Agent
beacon status --agent agent-id
```

## 📖 Dokumentation

- [Einstiegs-Tutorial](TUTORIALS/getting-started.md)
- [API-Referenz](docs/API.md)
- [Konfigurationsanleitung](docs/CONFIGURATION.md)
- [Integrationsbeispiele](docs/INTEGRATION.md)

## 🤝 Beitragen

Beiträge sind willkommen! Siehe unseren [Beitragsleitfaden](CONTRIBUTING.md) für Details.

### Schnellstart

1. Repository forken
2. Feature-Branch erstellen: `git checkout -b feature/my-feature`
3. Änderungen vornehmen
4. Tests ausführen: `cargo test`
5. PR einreichen

## 📜 Lizenz

Dieses Projekt ist unter der MIT-Lizenz lizenziert - siehe [LICENSE](LICENSE) für Details.

## 🏆 Bounties

Dieses Projekt nimmt am RustChain-Bounty-Programm teil:

- **Dokumentation**: 2-5 RTC pro Verbesserung
- **Funktionen**: 5-20 RTC pro Funktion
- **Bugfixes**: 3-10 RTC pro Fix

Bounties mit Wallet beanspruchen: `joshualover-dev`

Siehe [rustchain-bounties](https://github.com/Scottcjn/rustchain-bounties) für verfügbare Möglichkeiten.

## 🔗 Links

- [RustChain](https://github.com/Scottcjn/Rustchain)
- [Bounty-Programm](https://github.com/Scottcjn/rustchain-bounties)
- [Discord-Community](https://discord.gg/rustchain)

---

**Mit ❤️ vom RustChain-Team erstellt**
