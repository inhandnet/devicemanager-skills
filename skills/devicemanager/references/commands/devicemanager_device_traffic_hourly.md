## devicemanager device traffic hourly

Query hourly traffic for a device

```
devicemanager device traffic hourly <device-id> [flags]
```

### Examples

```
  # Last 24 hours (default)
  devicemanager device traffic hourly <device-id>

  # Custom date range (max 6 days)
  devicemanager device traffic hourly <device-id> --after 2026-04-25 --before 2026-04-27
```

### Options

```
      --after string    Start date (YYYY-MM-DD)
      --before string   End date (YYYY-MM-DD, max 6 days from after)
  -h, --help            help for hourly
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
