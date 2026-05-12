## devicemanager device get

Get device details

```
devicemanager device get <device-id> [flags]
```

### Examples

```
  # Get full device details
  devicemanager device get 5d6349d6335c8c000178a194
```

### Options

```
  -h, --help   help for get
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
