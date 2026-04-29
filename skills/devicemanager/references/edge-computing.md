# 边缘计算管理

Device Manager 的边缘计算功能，包括引擎管理、应用管理、版本部署和远程控制。

## 概念

- **Edge Agent（引擎）**：运行在设备上的边缘计算运行时环境
- **Edge App（应用）**：运行在引擎之上的边缘计算应用程序
- **Version（版本）**：应用的特定发布版本，可部署到设备
- **Config（配置）**：应用版本的运行时配置，可独立部署
- **Control（控制）**：远程启动/停止/重启设备上的边缘应用

## 典型工作流

### 1. 部署新应用到设备

```
步骤 1：确认引擎已安装
  devicemanager edge agent list
  devicemanager edge agent devices <agent-id>  # 查看哪些设备装了引擎

步骤 2：创建应用
  devicemanager edge app create --name "my-app" --description "..."

步骤 3：上传应用版本
  devicemanager edge version upload --app <app-id> <file>

步骤 4：部署版本到设备
  devicemanager edge version deploy <app-id> <version> --device <device-id>
  # 或按组部署
  devicemanager edge version deploy <app-id> <version> --group <group-id>

步骤 5：验证部署状态
  devicemanager edge agent devices <agent-id> --status running
```

### 2. 更新应用配置

```
步骤 1：查看现有配置
  devicemanager edge config list <app-id>

步骤 2：创建新配置
  devicemanager edge config create --version <version> --content '{"key":"value"}'

步骤 3：部署配置
  devicemanager edge config deploy <app-id> <config-id> --device <device-id>
```

### 3. 远程控制应用

```bash
# 启动应用
devicemanager edge control start <device-id> <app-id>

# 停止应用
devicemanager edge control stop <device-id> <app-id>

# 重启应用
devicemanager edge control restart <device-id> <app-id>
```

> **注意**：远程控制操作需要设备在线。执行前确认设备在线状态。

### 4. 管理引擎

```bash
# 上传新引擎版本
devicemanager edge agent upload <file> --description "v2.0 with Python 3.11"

# 查看引擎部署情况
devicemanager edge agent devices <agent-id>

# 按状态过滤
devicemanager edge agent devices <agent-id> --status running
```

## 注意事项

- 部署版本/配置到设备前，确保设备已安装对应的边缘引擎
- 大规模部署建议先在单台设备验证，成功后再按组批量部署
- 远程控制（start/stop/restart）需要设备在线
- 删除应用前确认没有设备正在运行该应用
