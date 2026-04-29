# 固件升级

设备固件管理和 OTA 升级操作指南。

## 查看可用固件

```bash
# 列出所有固件
devicemanager firmware list

# 按型号过滤
devicemanager firmware list --model IR915
```

## 单台设备升级

```
步骤 1：确认设备当前固件版本
  devicemanager device get <device-id>

步骤 2：查找目标固件
  devicemanager firmware list --model <设备型号>

步骤 3：确认升级计划
  向用户确认：目标设备、当前版本、目标版本

步骤 4：执行升级
  devicemanager firmware upgrade <device-id> --firmware-id <firmware-id>
```

## 批量升级

```
步骤 1：查看固件信息
  devicemanager firmware list --model <model>

步骤 2：添加设备到升级任务
  # 按设备组添加
  devicemanager firmware devices add <firmware-id> --group <group-id>

步骤 3：查看升级进度
  devicemanager firmware devices list <firmware-id>

步骤 4：处理失败设备
  # 查看失败设备后可移除并重试
  devicemanager firmware devices remove <job-id> <device-id>
  devicemanager firmware devices add <firmware-id> <device-id>
```

## 上传新固件

```
步骤 1：创建固件记录
  devicemanager firmware create \
    --fid <固件唯一标识> \
    --name "IR915 V2.0.1" \
    --version "2.0.1" \
    --model IR915

步骤 2：上传固件文件
  devicemanager firmware upload <firmware-id> <file-path>
```

## 注意事项

- **升级前必须确认**：向用户确认目标设备和固件版本，升级过程中设备会重启
- **设备必须在线**：离线设备无法接收升级指令
- **先单台后批量**：先在一台设备上验证升级成功，再批量推送
- **不要跨型号升级**：固件与设备型号必须匹配
- **升级期间不要断电**：升级过程中断电可能导致设备变砖
- **批量升级分批执行**：每批不超过 50 台设备，观察结果后再继续
- 升级完成后设备会自动重启，短暂离线属正常现象
