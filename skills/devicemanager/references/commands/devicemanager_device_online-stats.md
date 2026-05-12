## devicemanager device online-stats

Query device online statistics

### Synopsis

Query online statistics for devices. Fetches the device list first, then
queries online stats for those devices and merges the results.
Supports pagination and device filtering.

```
devicemanager device online-stats [flags]
```

### Examples

```
  # Query online stats for all devices
  devicemanager device online-stats --start-time 2026-05-01 --end-time 2026-05-09

  # Filter by device name
  devicemanager device online-stats --start-time 2026-05-01 --end-time 2026-05-09 --name router

  # Pagination
  devicemanager device online-stats --start-time 2026-05-01 --end-time 2026-05-09 --limit 50
```

### Options

```
      --cursor int          Skip N items (pagination offset)
      --end-time string     End date (YYYY-MM-DD, set to 23:59:59; if today, use current time) (required)
  -h, --help                help for online-stats
      --limit int           Number of items per page (default 20)
      --model string        Filter by device model
      --name string         Filter by device name
      --online string       Filter by online status (0=offline, 1=online)
      --start-time string   Start date inclusive (YYYY-MM-DD) (required)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
