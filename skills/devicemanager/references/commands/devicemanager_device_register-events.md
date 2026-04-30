## devicemanager device register-events

List device registration events by serial number

```
devicemanager device register-events <serial-number> [flags]
```

### Examples

```
  # View registration history for a device
  devicemanager device register-events GL5021937123456
```

### Options

```
      --cursor int    Skip N items (pagination offset)
  -h, --help          help for register-events
      --limit int     Number of items per page (default 20)
      --verbose int   Detail level (1-100, higher = more fields) (default 10)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
