# Device Manager Skills

[Agent Skills](https://agentskills.io) for managing Device Manager platform via `devicemanager` CLI.

## Features

- **设备管理** — 查询设备列表、在线状态、信号质量、连接客户端、流量统计
- **设备诊断** — 离线排查、信号分析、远程重启、强制踢下线
- **设备配置** — 获取/下发设备配置
- **设备分组** — 创建、管理设备组，批量添加/移除设备
- **远程隧道** — 创建隧道、连接/断开、端口转发
- **DRC 模板** — 配置模板管理，批量下发配置到设备
- **边缘计算** — 管理边缘引擎、应用、版本、配置，远程启停控制
- **固件升级** — 固件管理、单台/批量 OTA 升级

## Prerequisites

- Device Manager 平台账号
- `devicemanager` CLI（技能首次使用时会自动安装，或从 [devicemanager-cli](https://github.com/inhandnet/devicemanager-cli) 手动安装）

## Installation

### Claude Code

```bash
# CLI
claude skill add --source github:inhandnet/devicemanager-skills

# Desktop / Web / IDE Extension
# Settings → Skills → Add Skill → github:inhandnet/devicemanager-skills
```

### Codex CLI

```bash
codex skill add github:inhandnet/devicemanager-skills
```

## Usage

技能会自动识别用户意图并激活：

```
> 查看所有在线设备
> 帮我看一下 IR915L 的信号质量
> 把这批设备加入 "华东区" 分组
> 给设备创建一个远程隧道
> 部署边缘应用到设备
```

也可以通过 `/devicemanager` 显式调用：

```
> /devicemanager 列出所有离线设备
```

## Troubleshooting

### `devicemanager: command not found`

手动安装 CLI：

```bash
# macOS / Linux
go install github.com/inhandnet/devicemanager-cli/cmd/devicemanager@latest

# 或下载预编译二进制
# https://github.com/inhandnet/devicemanager-cli/releases
```

### 认证失败

```bash
devicemanager auth login
```

## Skills

| Skill | Description |
|-------|-------------|
| `devicemanager` | Device Manager 平台管理 |
