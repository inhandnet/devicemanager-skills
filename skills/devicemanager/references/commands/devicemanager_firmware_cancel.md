## devicemanager firmware cancel

Cancel a firmware upgrade task for a device

### Synopsis

Cancel a device's firmware upgrade task. The firmware-id can be found via 'firmware list'.

```
devicemanager firmware cancel <firmware-id> <device-id> [flags]
```

### Examples

```
  # Cancel upgrade for a device
  devicemanager firmware cancel <firmware-id> <device-id>

  # Find firmware IDs first
  devicemanager firmware list
```

### Options

```
  -h, --help   help for cancel
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
