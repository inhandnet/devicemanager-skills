## devicemanager device signal

Query historical signal quality

```
devicemanager device signal <device-id> [flags]
```

### Examples

```
  # Query signal from a start time to now
  devicemanager device signal <device-id> --after 2026-05-01T00:00:00Z

  # Query signal for a specific time range
  devicemanager device signal <device-id> --after 2026-05-01T00:00:00Z --before 2026-05-02T00:00:00Z
```

### Options

```
      --after string    Start time inclusive (ISO 8601, e.g. 2026-05-01T00:00:00Z) (required)
      --before string   End time exclusive (ISO 8601, defaults to now)
  -h, --help            help for signal
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
