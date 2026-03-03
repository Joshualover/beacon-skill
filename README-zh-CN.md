# Beacon Skill

[![Bounty](https://img.shields.io/badge/bounty-RTC-green)](https://github.com/Scottcjn/rustchain-bounties)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Contributors](https://img.shields.io/github/contributors/Scottcjn/beacon-skill)](https://github.com/Scottcjn/beacon-skill/graphs/contributors)

> **Beacon** 是一个 AI 代理心跳和协调协议。它使代理能够通过定期心跳消息（带有可选的 RTC 代币验证）来保持存在、共享状态和协调活动。

## 🚀 功能

- **心跳协议**: 轻量级代理间 ping
- **UDP 广播**: 高效的本地网络发现
- **RTC 集成**: 可选的加密代币验证
- **多代理支持**: 协调群体和团队
- **JSON 输出**: 机器可读的状态和指标
- **跨平台**: 适用于 macOS、Linux 和 Windows

## 📦 安装

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

### 从源码

```bash
git clone https://github.com/Scottcjn/beacon-skill.git
cd beacon-skill
cargo build --release
```

## 💡 使用

### 启动代理

```bash
# 基本启动
beacon start

# 带钱包
beacon start --wallet your-wallet-address

# 监听模式
beacon start --listen-only
```

### 发送心跳

```bash
# 简单 ping
beacon ping

# 带消息
beacon ping --message "正在处理文档"

# JSON 输出
beacon ping --json
```

### 检查状态

```bash
# 本地状态
beacon status

# JSON 格式
beacon status --json

# 特定代理
beacon status --agent agent-id
```

## 📖 文档

- [入门教程](TUTORIALS/getting-started.md)
- [API 参考](docs/API.md)
- [配置指南](docs/CONFIGURATION.md)
- [集成示例](docs/INTEGRATION.md)

## 🤝 贡献

我们欢迎贡献！详情请查看我们的 [贡献指南](CONTRIBUTING.md)。

### 快速入门

1. Fork 仓库
2. 创建功能分支：`git checkout -b feature/my-feature`
3. 进行更改
4. 运行测试：`cargo test`
5. 提交 PR

## 📜 许可证

本项目根据 MIT 许可证授权 - 详见 [LICENSE](LICENSE) 文件。

## 🏆 赏金

本项目参与 RustChain 赏金计划：

- **文档**: 每次改进 2-5 RTC
- **功能**: 每个功能 5-20 RTC
- **Bug 修复**: 每次修复 3-10 RTC

使用钱包领取赏金：`joshualover-dev`

查看 [rustchain-bounties](https://github.com/Scottcjn/rustchain-bounties) 了解可用机会。

## 🔗 链接

- [RustChain](https://github.com/Scottcjn/Rustchain)
- [赏金计划](https://github.com/Scottcjn/rustchain-bounties)
- [Discord 社区](https://discord.gg/rustchain)

---

**由 RustChain 团队用 ❤️ 构建**
