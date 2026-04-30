## devicemanager device online-events

List device online/offline event timeline

```
devicemanager device online-events <device-id> [flags]
```

### Examples

```
  # Show online/offline events for the last 24 hours
  devicemanager device online-events 639acc6e078a3d0001be2963 \
    --start-time 2026-04-29 --end-time 2026-04-30

  # Investigate overnight disconnections
  devicemanager device online-events 639acc6e078a3d0001be2963 \
    --start-time 2026-04-29T22:00:00 --end-time 2026-04-30T08:00:00
```

### Options

```
      --end-time string     End time (YYYY-MM-DD or ISO8601) (required)
  -h, --help                help for online-events
      --start-time string   Start time (YYYY-MM-DD or ISO8601) (required)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
