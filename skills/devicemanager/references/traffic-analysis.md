# 流量统计分析

查看设备流量使用情况，包括月度汇总和每日明细。

## 月度流量

```bash
devicemanager device traffic monthly --device <device-id1>,<device-id2>
```

- `--device` 必填，支持多个设备 ID（逗号分隔）
- 返回指定月份的流量汇总数据

## 每日流量

```bash
devicemanager device traffic daily
```

返回每日流量明细。

## 分析要点

### 流量异常排查

1. **流量突增**：
   - 对比历史同期数据，确认是否异常
   - 检查连接客户端 `devicemanager device clients list <id>`，是否有未知设备接入
   - 查看设备告警是否有异常上报

2. **流量为零**：
   - 确认设备是否在线
   - 检查 WAN 接口是否正常
   - 确认计费周期是否匹配

3. **流量超标**：
   - 查看流量趋势，定位高消耗时段
   - 检查客户端列表，识别高流量用户/设备
   - 考虑调整 QoS 或带宽限制配置

### 批量流量对比

查看多台设备的月度流量，找出流量异常的设备：

```bash
devicemanager device traffic monthly --device <id1>,<id2>,<id3>
```

## 注意事项

- 流量数据有一定延迟，通常非实时
- 月度流量统计以自然月为周期
- 流量数据为设备上报的统计值，可能与运营商计费有差异
