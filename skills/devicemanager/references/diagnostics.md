# 设备离线诊断

设备掉线/断网/连不上时的排查流程。

## 诊断步骤

### 1. 确认设备状态

```bash
devicemanager device get <device-id> --verbose 100
```

关注字段：
- `online`：当前是否在线
- `lastSeen` / `updatedAt`：最后在线时间
- `model`：设备型号
- `firmware`：固件版本

### 2. 查看信号质量（蜂窝设备）

```bash
devicemanager device signal <device-id> --after <time> --before <time>
```

信号趋势可以反映是否因信号衰减导致断线。

### 3. 查看告警记录

```bash
devicemanager device alert <device-id>
```

检查是否有离线告警、链路切换告警等。

### 4. 查看连接客户端

```bash
devicemanager device clients list <device-id>
```

如果设备在线但下挂客户端连不上，可能是 LAN 侧问题。

### 5. 检查设备配置

```bash
devicemanager device config get <device-id>
```

确认配置是否正确，特别是 WAN 接口、APN、DHCP 等关键配置。

### 6. 远程重启（需要设备在线）

确认设备在线后，可尝试远程重启：

```bash
devicemanager device reboot <device-id>
```

> **注意**：重启前必须获得用户确认。重启后设备会短暂离线，等待重新上线。

### 7. 强制断开重连

如果设备状态异常（显示在线但无法通信），可强制踢下线让其重连：

```bash
devicemanager device kick <device-id>
```

## 离线设备的排查建议

设备离线时，远程操作（reboot、kick、config set）均无法执行。引导用户：

1. 确认设备供电正常
2. 检查 SIM 卡（蜂窝设备）或网线（有线设备）
3. 检查天线连接
4. 本地登录设备 Web 管理页面排查
5. 如有条件，尝试本地重启设备

## 批量离线排查

查找所有离线设备：

```bash
devicemanager device list --online false
```

按型号过滤离线设备：

```bash
devicemanager device list --online false --model IR915
```
