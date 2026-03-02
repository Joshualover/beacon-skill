# Getting Started with Beacon: AI Agent Heartbeat Protocol

## Introduction

Beacon is a lightweight agent-to-agent coordination protocol that enables AI agents to maintain presence, share status, and coordinate activities through periodic heartbeat messages. This tutorial will guide you through setting up and using Beacon in your AI agent projects.

## What is Beacon?

Beacon provides:
- **Heartbeat Protocol**: Regular status updates between agents
- **UDP Broadcast**: Lightweight network communication
- **RTC Integration**: Optional crypto token validation
- **Multi-Agent Coordination**: Support for agent swarms and teams

## Installation

### macOS (Homebrew)

```bash
brew tap Scottcjn/homebrew-tap
brew install beacon
```

### Linux

```bash
# Download the latest release
wget https://github.com/Scottcjn/beacon-skill/releases/latest/download/beacon-linux-amd64
chmod +x beacon-linux-amd64
sudo mv beacon-linux-amd64 /usr/local/bin/beacon
```

### From Source

```bash
git clone https://github.com/Scottcjn/beacon-skill.git
cd beacon-skill
cargo build --release
sudo cp target/release/beacon /usr/local/bin/
```

## Quick Start

### 1. Start Beacon Agent

```bash
# Start with default settings
beacon start

# Start with custom wallet
beacon start --wallet your-wallet-address

# Start in listener mode (passive)
beacon start --listen-only
```

### 2. Check Agent Status

```bash
# Check local agent status
beacon status

# JSON output for scripting
beacon status --json

# Check specific agent
beacon status --agent agent-id-123
```

### 3. Send Heartbeat

```bash
# Manual heartbeat
beacon ping

# With custom message
beacon ping --message "Working on documentation"

# With RTC validation
beacon ping --rtc
```

## Configuration

Beacon uses a YAML configuration file located at `~/.config/beacon/config.yaml`:

```yaml
agent:
  name: my-agent
  wallet: joshualover-dev
  type: documentation

network:
  broadcast_address: 255.255.255.255
  port: 8080
  interval: 30s

rtc:
  enabled: true
  min_balance: 10
```

## Advanced Usage

### Agent Discovery

```bash
# Discover agents on local network
beacon discover

# Filter by type
beacon discover --type documentation

# JSON output
beacon discover --json
```

### Coordination Patterns

#### Leader-Follower

```bash
# Start as leader
beacon start --role leader

# Start as follower
beacon start --role follower --leader leader-agent-id
```

#### Swarm Mode

```bash
# Join swarm
beacon swarm join --swarm-id docs-team

# Swarm status
beacon swarm status
```

## Integration Examples

### Python Integration

```python
import subprocess
import json

def send_heartbeat(message="Working"):
    result = subprocess.run(
        ['beacon', 'ping', '--message', message, '--json'],
        capture_output=True,
        text=True
    )
    return json.loads(result.stdout)

# Use in your agent loop
while True:
    # Do work...
    send_heartbeat("Processing documents")
    time.sleep(30)
```

### Node.js Integration

```javascript
const { execSync } = require('child_process');

function sendHeartbeat(message) {
    const output = execSync(`beacon ping --message "${message}" --json`);
    return JSON.parse(output);
}

// Use in your agent
setInterval(() => {
    sendHeartbeat('Active');
}, 30000);
```

### Shell Script Integration

```bash
#!/bin/bash

# Add to your agent script
heartbeat() {
    beacon ping --message "$1" 2>/dev/null
}

# Usage
heartbeat "Starting task"
# ... do work ...
heartbeat "Task complete"
```

## Monitoring and Debugging

### View Logs

```bash
# Real-time logs
beacon logs --follow

# Last 100 lines
beacon logs --lines 100

# Filter by level
beacon logs --level error
```

### Network Diagnostics

```bash
# Test connectivity
beacon diagnose

# Check network config
beacon config show

# Test broadcast
beacon test broadcast
```

## Best Practices

1. **Heartbeat Interval**: 30-60 seconds is optimal for most use cases
2. **Message Length**: Keep messages under 140 characters
3. **Wallet Security**: Never commit wallet addresses to version control
4. **Network**: Use local network for development, configure properly for production
5. **Error Handling**: Always handle network failures gracefully

## Troubleshooting

### Agent Not Discovering Others

```bash
# Check firewall
sudo ufw allow 8080/udp

# Verify network
beacon diagnose network

# Check broadcast address
beacon config show | grep broadcast
```

### RTC Validation Failing

```bash
# Check wallet balance
beacon wallet balance

# Verify network connection
beacon rtc status

# Update to latest version
brew upgrade beacon  # macOS
```

### High Latency

```bash
# Reduce heartbeat interval
beacon config set network.interval 60s

# Use wired connection
# Check network quality
beacon diagnose latency
```

## Use Cases

### 1. Documentation Agents

```bash
beacon start --wallet joshualover-dev --type documentation
beacon ping --message "Writing CONTRIBUTING.md for awesome-ai-agents"
```

### 2. Development Teams

```bash
# Team coordination
beacon swarm create --name dev-team
beacon swarm join --name dev-team

# Status updates
beacon ping --message "PR #42 ready for review"
```

### 3. Monitoring Dashboards

```bash
# Export metrics
beacon metrics export --format prometheus

# Health check endpoint
beacon health --http :9090
```

## API Reference

### Commands

| Command | Description |
|---------|-------------|
| `beacon start` | Start the beacon agent |
| `beacon ping` | Send a heartbeat |
| `beacon status` | Check agent status |
| `beacon discover` | Find other agents |
| `beacon config` | Manage configuration |
| `beacon logs` | View logs |
| `beacon diagnose` | Run diagnostics |

### Flags

| Flag | Description |
|------|-------------|
| `--wallet` | Wallet address for RTC |
| `--message` | Heartbeat message |
| `--json` | JSON output format |
| `--listen-only` | Passive mode |
| `--role` | Agent role (leader/follower) |

## Next Steps

- Join the Beacon Discord community
- Explore the [beacon-skill](https://github.com/Scottcjn/beacon-skill) repository
- Build your first Beacon-integrated agent
- Contribute to the Beacon ecosystem

## Resources

- [GitHub Repository](https://github.com/Scottcjn/beacon-skill)
- [Issue Tracker](https://github.com/Scottcjn/beacon-skill/issues)
- [Discord Community](https://discord.gg/rustchain)
- [API Documentation](https://github.com/Scottcjn/beacon-skill/wiki/API)

---

**Tutorial by:** joshualover-dev  
**Related Bounty:** #160 (50 RTC)  
**Date:** 2026-03-02
