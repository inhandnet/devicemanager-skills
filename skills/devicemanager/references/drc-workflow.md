# DRC 配置模板管理

DRC（Device Remote Configuration）用于创建配置模板并批量下发到设备。

## 概念

- **DRC 模板**：一套预定义的设备配置，绑定到特定设备型号
- **模板分配**：将设备加入模板，平台会自动将模板配置推送到设备
- **任务状态**：设备接收并应用模板配置后的执行状态

## 典型工作流

### 1. 创建并下发配置模板

```
步骤 1：确认设备型号
  devicemanager device list --model <model>

步骤 2：创建 DRC 模板
  devicemanager drc create --name "华东区统一配置" --model IR915 --content '{"wan":{"mode":"dhcp"}}'

步骤 3：分配设备到模板
  # 按单台设备
  devicemanager drc devices add <template-id> <device-id1> <device-id2>
  # 按设备组
  devicemanager drc devices add <template-id> --group <group-id>

步骤 4：检查下发状态
  devicemanager drc devices list <template-id>
  devicemanager drc devices list <template-id> --status failed  # 查看失败的
```

### 2. 查看和管理已有模板

```bash
# 列出所有模板
devicemanager drc list

# 按型号过滤
devicemanager drc list --model IR915

# 查看模板详情（含配置内容）
devicemanager drc get <template-id>
```

### 3. 处理下发失败

```bash
# 查看失败设备
devicemanager drc devices list <template-id> --status failed

# 重试单台设备
devicemanager drc devices restart <template-id> <device-id>

# 移除并重新添加
devicemanager drc devices remove <template-id> <device-id>
devicemanager drc devices add <template-id> <device-id>
```

## 注意事项

- 模板绑定特定型号，不能跨型号使用
- `--content` 必须是合法 JSON，建议先用 `devicemanager device config get` 获取当前配置作为参考
- 批量分配设备时，每批不超过 50 台
- 高风险配置（如 WAN 接口修改）先在单台设备验证成功后再批量推送
- 删除模板前确认已移除所有分配的设备
