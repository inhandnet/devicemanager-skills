## devicemanager device kick

Force disconnect a device

### Synopsis

Force disconnect a device from the platform. The device will attempt to reconnect automatically.

```
devicemanager device kick <device-id> [flags]
```

### Examples

```
  devicemanager device kick 5d6349d6335c8c000178a194
```

### Options

```
  -h, --help   help for kick
  -y, --yes    Skip confirmation prompt
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
