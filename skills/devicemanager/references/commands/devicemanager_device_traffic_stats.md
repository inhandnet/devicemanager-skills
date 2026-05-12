## devicemanager device traffic stats

Query device traffic statistics

### Synopsis

Query traffic statistics for devices. Fetches the device list first, then
queries traffic data for those devices and merges the results.
Supports pagination and device filtering.

```
devicemanager device traffic stats [flags]
```

### Examples

```
  # Query traffic stats for all devices
  devicemanager device traffic stats --after 2026-05-01 --before 2026-05-09

  # Filter by device name
  devicemanager device traffic stats --after 2026-05-01 --before 2026-05-09 --name router

  # Only online devices
  devicemanager device traffic stats --after 2026-05-01 --before 2026-05-09 --online 1
```

### Options

```
      --after string    Start date inclusive (YYYY-MM-DD) (required)
      --before string   End date exclusive (YYYY-MM-DD) (required)
      --cursor int      Skip N items (pagination offset)
  -h, --help            help for stats
      --limit int       Number of items per page (default 20)
      --model string    Filter by device model
      --name string     Filter by device name
      --online string   Filter by online status (0=offline, 1=online)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
