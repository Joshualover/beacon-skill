# Beacon Skill

[![Bounty](https://img.shields.io/badge/bounty-RTC-green)](https://github.com/Scottcjn/rustchain-bounties)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Contributors](https://img.shields.io/github/contributors/Scottcjn/beacon-skill)](https://github.com/Scottcjn/beacon-skill/graphs/contributors)

> **Beacon** — это протокол сердцебиения и координации ИИ-агентов. Он позволяет агентам поддерживать присутствие, обмениваться статусом и координировать действия через периодические сообщения сердцебиения с опциональной валидацией RTC-токенов.

## 🚀 Возможности

- **Протокол Сердцебиения**: Лёгкие пинги между агентами
- **UDP Вещание**: Эффективное обнаружение локальной сети
- **Интеграция RTC**: Опциональная валидация крипто-токенов
- **Поддержка Мульти-Агентов**: Координация роев и команд
- **JSON Вывод**: Статус и метрики, читаемые машиной
- **Кроссплатформенность**: Работает на macOS, Linux и Windows

## 📦 Установка

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

### Из Исходников

```bash
git clone https://github.com/Scottcjn/beacon-skill.git
cd beacon-skill
cargo build --release
```

## 💡 Использование

### Запуск Агента

```bash
# Базовый запуск
beacon start

# С кошельком
beacon start --wallet your-wallet-address

# Режим слушателя
beacon start --listen-only
```

### Отправить Сердцебиение

```bash
# Простой пинг
beacon ping

# С сообщением
beacon ping --message "Работаю над документацией"

# JSON вывод
beacon ping --json
```

### Проверить Статус

```bash
# Локальный статус
beacon status

# JSON формат
beacon status --json

# Конкретный агент
beacon status --agent agent-id
```

## 📖 Документация

- [Учебник по Началу Работы](TUTORIALS/getting-started.md)
- [Справочник API](docs/API.md)
- [Руководство по Настройке](docs/CONFIGURATION.md)
- [Примеры Интеграции](docs/INTEGRATION.md)

## 🤝 Вклад

Вклады приветствуются! См. наше [Руководство по Вкладу](CONTRIBUTING.md) для деталей.

### Быстрый Старт

1. Форкните репозиторий
2. Создайте ветку функции: `git checkout -b feature/my-feature`
3. Внесите изменения
4. Запустите тесты: `cargo test`
5. Отправьте PR

## 📜 Лицензия

Этот проект лицензирован под лицензией MIT - см. файл [LICENSE](LICENSE) для деталей.

## 🏆 Баунти

Этот проект участвует в программе баунти RustChain:

- **Документация**: 2-5 RTC за улучшение
- **Функции**: 5-20 RTC за функцию
- **Исправления Багов**: 3-10 RTC за исправление

Требуйте баунти с кошельком: `joshualover-dev`

См. [rustchain-bounties](https://github.com/Scottcjn/rustchain-bounties) для доступных возможностей.

## 🔗 Ссылки

- [RustChain](https://github.com/Scottcjn/Rustchain)
- [Программа Баунти](https://github.com/Scottcjn/rustchain-bounties)
- [Discord Сообщество](https://discord.gg/rustchain)

---

**Создано с ❤️ командой RustChain**
