# 设备配置管理

获取和下发单台设备配置的操作指南。

## 获取当前配置

```bash
devicemanager device config get <device-id>
```

返回设备当前运行配置的完整 JSON。

## 下发配置

```bash
devicemanager device config set <device-id> --content '<json>'
```

### 配置下发工作流

```
步骤 1：获取当前配置
  devicemanager device config get <device-id>

步骤 2：分析当前配置，确认要修改的部分

步骤 3：构造变更 JSON
  - 基于当前配置修改，不要从零开始构造
  - 只包含需要变更的字段

步骤 4：确认变更内容
  向用户展示即将变更的内容，获得确认

步骤 5：下发配置
  devicemanager device config set <device-id> --content '<json>'

步骤 6：验证
  等待片刻后重新获取配置，确认变更已生效
  devicemanager device config get <device-id>
```

## 注意事项

- **写操作前先 GET**：必须先获取当前配置，了解现有结构和字段名
- **不要猜字段名**：不同型号的配置结构可能不同
- **高风险配置要谨慎**：修改 WAN 接口、管理接口等关键配置可能导致设备失联
- **先单台后批量**：如需批量下发相同配置，先在单台验证成功后再用 DRC 模板批量推送
- `--content` 必须是合法 JSON 字符串
- 设备必须在线才能下发配置
