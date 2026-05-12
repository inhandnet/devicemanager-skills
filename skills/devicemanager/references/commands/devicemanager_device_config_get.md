## devicemanager device config get

Get device running configuration

### Synopsis

Fetch the device's running configuration. By default, it first sends a
"GET RUNNING CONFIG" task to the device to retrieve the latest config.
If the device is offline or the task fails, the last known config is returned.
Use --skip-refresh to skip the task and return the cached config directly.

```
devicemanager device config get <device-id> [flags]
```

### Examples

```
  # Get latest config (sends task to device first)
  devicemanager device config get <device-id>

  # Get cached config without refreshing
  devicemanager device config get <device-id> --skip-refresh
```

### Options

```
  -h, --help           help for get
      --skip-refresh   Skip refreshing config from device, return cached config
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
