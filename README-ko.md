# Beacon Skill

[![Bounty](https://img.shields.io/badge/bounty-RTC-green)](https://github.com/Scottcjn/rustchain-bounties)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Contributors](https://img.shields.io/github/contributors/Scottcjn/beacon-skill)](https://github.com/Scottcjn/beacon-skill/graphs/contributors)

> **Beacon** 은 AI 에이전트 하트비트 및 조정 프로토콜입니다. 에이전트가 존재를 유지하고, 상태를 공유하며, 옵션 RTC 토큰 검증과 함께 정기적인 하트비트 메시지를 통해 활동을 조정할 수 있게 합니다.

## 🚀 기능

- **하트비트 프로토콜**: 경량 에이전트 간 ping
- **UDP 브로드캐스트**: 효율적인 로컬 네트워크 검색
- **RTC 통합**: 옵션 암호화 토큰 검증
- **멀티 에이전트 지원**: 무리 및 팀 조정
- **JSON 출력**: 기계 판독 가능한 상태 및 지표
- **크로스 플랫폼**: macOS, Linux, Windows 에서 작동

## 📦 설치

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

### 소스에서

```bash
git clone https://github.com/Scottcjn/beacon-skill.git
cd beacon-skill
cargo build --release
```

## 💡 사용법

### 에이전트 시작

```bash
# 기본 시작
beacon start

# 지갑 포함
beacon start --wallet your-wallet-address

# 리스너 모드
beacon start --listen-only
```

### 하트비트 보내기

```bash
# 단순 ping
beacon ping

# 메시지 포함
beacon ping --message "문서 작업 중"

# JSON 출력
beacon ping --json
```

### 상태 확인

```bash
# 로컬 상태
beacon status

# JSON 형식
beacon status --json

# 특정 에이전트
beacon status --agent agent-id
```

## 📖 문서

- [시작 튜토리얼](TUTORIALS/getting-started.md)
- [API 참조](docs/API.md)
- [설정 가이드](docs/CONFIGURATION.md)
- [통합 예시](docs/INTEGRATION.md)

## 🤝 기여

기여를 환영합니다! 자세한 내용은 [기여 가이드](CONTRIBUTING.md) 를 참조하세요.

### 빠른 시작

1. 저장소 포크
2. 기능 브랜치 생성: `git checkout -b feature/my-feature`
3. 변경 사항 작성
4. 테스트 실행: `cargo test`
5. PR 제출

## 📜 라이선스

이 프로젝트는 MIT 라이선스에 따라 라이선스가 부여됩니다 - 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

## 🏆 바운티

이 프로젝트는 RustChain 바운티 프로그램에 참여합니다:

- **문서**: 개선당 2-5 RTC
- **기능**: 기능당 5-20 RTC
- **버그 수정**: 수정당 3-10 RTC

지갑으로 바운티 청구: `joshualover-dev`

사용 가능한 기회는 [rustchain-bounties](https://github.com/Scottcjn/rustchain-bounties) 를 참조하세요.

## 🔗 링크

- [RustChain](https://github.com/Scottcjn/Rustchain)
- [바운티 프로그램](https://github.com/Scottcjn/rustchain-bounties)
- [Discord 커뮤니티](https://discord.gg/rustchain)

---

**RustChain 팀이 ❤️ 으로 구축**
