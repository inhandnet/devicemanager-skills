## devicemanager device online-stats

Query device online statistics

```
devicemanager device online-stats [flags]
```

### Examples

```
  # Query online stats for specific devices in the last 7 days
  devicemanager device online-stats --device-id 639acc6e078a3d0001be2963 \
    --start-time 2026-04-23 --end-time 2026-04-30

  # Query multiple devices
  devicemanager device online-stats \
    --device-id 639acc6e078a3d0001be2963 \
    --device-id 5d6349d6335c8c000178a194 \
    --start-time 2026-04-23 --end-time 2026-04-30
```

### Options

```
      --device-id strings   Device ID(s) to query (required, repeatable)
      --end-time string     End date (YYYY-MM-DD) (required)
  -h, --help                help for online-stats
      --start-time string   Start date (YYYY-MM-DD) (required)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
