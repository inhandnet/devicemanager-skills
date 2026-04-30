## devicemanager firmware upgrade

Upgrade a single device

```
devicemanager firmware upgrade <device-id> [flags]
```

### Examples

```
  devicemanager firmware upgrade <device-id> --firmware-id <id> --timeout 600
```

### Options

```
      --device-name string   Device name
      --firmware-id string   Firmware ID (required)
  -h, --help                 help for upgrade
      --timeout int          Upgrade timeout (seconds)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
