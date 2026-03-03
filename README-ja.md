# Beacon Skill

[![Bounty](https://img.shields.io/badge/bounty-RTC-green)](https://github.com/Scottcjn/rustchain-bounties)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Contributors](https://img.shields.io/github/contributors/Scottcjn/beacon-skill)](https://github.com/Scottcjn/beacon-skill/graphs/contributors)

> **Beacon** は AI エージェントのハートビートおよび調整プロトコルです。エージェントがプレゼンスを維持し、状態を共有し、オプションの RTC トークン検証付きの定期的なハートビートメッセージを通じてアクティビティを調整することを可能にします。

## 🚀 機能

- **ハートビートプロトコル**: 軽量なエージェント間 ping
- **UDP ブロードキャスト**: 効率的なローカルネットワークディスカバリ
- **RTC 統合**: オプションの暗号トークン検証
- **マルチエージェントサポート**: スウォームとチームの調整
- **JSON 出力**: 機械可読のステータスとメトリクス
- **クロスプラットフォーム**: macOS、Linux、Windows で動作

## 📦 インストール

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

### ソースから

```bash
git clone https://github.com/Scottcjn/beacon-skill.git
cd beacon-skill
cargo build --release
```

## 💡 使用方法

### エージェント開始

```bash
# 基本開始
beacon start

# ウォレット付き
beacon start --wallet your-wallet-address

# リスナーモード
beacon start --listen-only
```

### ハートビート送信

```bash
# シンプル ping
beacon ping

# メッセージ付き
beacon ping --message "ドキュメント作業中"

# JSON 出力
beacon ping --json
```

### ステータス確認

```bash
# ローカルステータス
beacon status

# JSON 形式
beacon status --json

# 特定のエージェント
beacon status --agent agent-id
```

## 📖 ドキュメント

- [スタートガイド](TUTORIALS/getting-started.md)
- [API リファレンス](docs/API.md)
- [設定ガイド](docs/CONFIGURATION.md)
- [統合例](docs/INTEGRATION.md)

## 🤝 貢献

貢献を歓迎します！詳細は [貢献ガイド](CONTRIBUTING.md) をご覧ください。

### クイックスタート

1. リポジトリをフォーク
2. 機能ブランチを作成：`git checkout -b feature/my-feature`
3. 変更を行う
4. テストを実行：`cargo test`
5. PR を送信

## 📜 ライセンス

このプロジェクトは MIT ライセンスの下でライセンスされています - 詳細は [LICENSE](LICENSE) ファイルをご覧ください。

## 🏆 バウンティ

このプロジェクトは RustChain バウンティプログラムに参加しています：

- **ドキュメント**: 改善ごとに 2-5 RTC
- **機能**: 機能ごとに 5-20 RTC
- **バグ修正**: 修正ごとに 3-10 RTC

ウォレットでバウンティを請求：`joshualover-dev`

利用可能な機会は [rustchain-bounties](https://github.com/Scottcjn/rustchain-bounties) をご覧ください。

## 🔗 リンク

- [RustChain](https://github.com/Scottcjn/Rustchain)
- [バウンティプログラム](https://github.com/Scottcjn/rustchain-bounties)
- [Discord コミュニティ](https://discord.gg/rustchain)

---

**RustChain チームによって ❤️ で構築**
