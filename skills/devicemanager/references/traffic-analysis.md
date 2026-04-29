# 流量统计分析

查看设备流量使用情况，包括月度汇总、每日明细和小时级明细。

## 月度流量

```bash
devicemanager device traffic monthly 202604 <device-id>
```

- 返回指定设备在指定月份的流量汇总数据

## 每日流量

```bash
devicemanager device traffic daily 202604 <device-id>
```

- 返回指定设备在指定月份内每日的流量明细

## 小时流量

```bash
# 默认查最近 24 小时
devicemanager device traffic hourly <device-id>

# 自定义日期范围（最大 6 天）
devicemanager device traffic hourly <device-id> --after 2026-04-25 --before 2026-04-27
```

- 返回指定设备的小时级流量数据
- 不传参数时默认查最近 24 小时
- `--after`/`--before` 指定日期范围，最大跨度 6 天

## 分析要点

### 流量异常排查

1. **流量突增**：
   - 对比历史同期数据，确认是否异常
   - 检查连接客户端 `devicemanager device clients list <id>`，是否有未知设备接入
   - 查看小时流量定位高消耗时段 `devicemanager device traffic hourly <id>`
   - 查看设备告警是否有异常上报

2. **流量为零**：
   - 确认设备是否在线
   - 检查 WAN 接口是否正常
   - 确认计费周期是否匹配

3. **流量超标**：
   - 查看日流量趋势，定位高消耗日期
   - 查看小时流量，定位高消耗时段
   - 检查客户端列表，识别高流量用户/设备
   - 考虑调整 QoS 或带宽限制配置

## 注意事项

- 流量数据有一定延迟，通常非实时
- 月度流量统计以自然月为周期
- 小时流量查询最大跨度 6 天
- 流量数据为设备上报的统计值，可能与运营商计费有差异
