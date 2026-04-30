## devicemanager device signal

Query historical signal quality

```
devicemanager device signal <device-id> [flags]
```

### Examples

```
  devicemanager device signal 5e6f222afbcf3e0001e133f4 \
    --after 2024-01-01T00:00:00Z --before 2024-01-02T00:00:00Z
```

### Options

```
      --after string    Start time (ISO 8601, e.g. 2024-01-01T00:00:00Z) (required)
      --before string   End time (ISO 8601, e.g. 2024-01-02T00:00:00Z) (required)
  -h, --help            help for signal
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
