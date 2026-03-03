# Beacon Skill

[![Bounty](https://img.shields.io/badge/bounty-RTC-green)](https://github.com/Scottcjn/rustchain-bounties)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Contributors](https://img.shields.io/github/contributors/Scottcjn/beacon-skill)](https://github.com/Scottcjn/beacon-skill/graphs/contributors)

> **Beacon** es un protocolo de latidos y coordinación de agentes de IA. Permite a los agentes mantener presencia, compartir estado y coordinar actividades a través de mensajes de latido periódicos con validación opcional de tokens RTC.

## 🚀 Características

- **Protocolo de Latidos**: Pings ligeros de agente a agente
- **Broadcast UDP**: Descubrimiento eficiente de red local
- **Integración RTC**: Validación opcional de tokens cripto
- **Soporte Multi-Agente**: Coordinar enjambres y equipos
- **Salida JSON**: Estado y métricas legibles por máquina
- **Multiplataforma**: Funciona en macOS, Linux y Windows

## 📦 Instalación

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

### Desde Fuente

```bash
git clone https://github.com/Scottcjn/beacon-skill.git
cd beacon-skill
cargo build --release
```

## 💡 Uso

### Iniciar Agente

```bash
# Inicio básico
beacon start

# Con billetera
beacon start --wallet your-wallet-address

# Modo escucha
beacon start --listen-only
```

### Enviar Latido

```bash
# Ping simple
beacon ping

# Con mensaje
beacon ping --message "Trabajando en documentación"

# Salida JSON
beacon ping --json
```

### Verificar Estado

```bash
# Estado local
beacon status

# Formato JSON
beacon status --json

# Agente específico
beacon status --agent agent-id
```

## 📖 Documentación

- [Tutorial de Inicio](TUTORIALS/getting-started.md)
- [Referencia API](docs/API.md)
- [Guía de Configuración](docs/CONFIGURATION.md)
- [Ejemplos de Integración](docs/INTEGRATION.md)

## 🤝 Contribuyendo

¡Las contribuciones son bienvenidas! Mira nuestra [Guía de Contribución](CONTRIBUTING.md) para detalles.

### Inicio Rápido

1. Haz fork del repositorio
2. Crea una rama de funcionalidad: `git checkout -b feature/my-feature`
3. Haz tus cambios
4. Ejecuta tests: `cargo test`
5. Envía un PR

## 📜 Licencia

Este proyecto está licenciado bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para detalles.

## 🏆 Bounties

Este proyecto participa en el programa de bounties de RustChain:

- **Documentación**: 2-5 RTC por mejora
- **Funcionalidades**: 5-20 RTC por funcionalidad
- **Corrección de Bugs**: 3-10 RTC por corrección

Reclama bounties con wallet: `joshualover-dev`

Mira [rustchain-bounties](https://github.com/Scottcjn/rustchain-bounties) para oportunidades disponibles.

## 🔗 Enlaces

- [RustChain](https://github.com/Scottcjn/Rustchain)
- [Programa de Bounties](https://github.com/Scottcjn/rustchain-bounties)
- [Comunidad Discord](https://discord.gg/rustchain)

---

**Construido con ❤️ por el Equipo RustChain**
