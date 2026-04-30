## devicemanager device create

Add a device

```
devicemanager device create [flags]
```

### Examples

```
  devicemanager device create --name "test-router" --serial-number GL5022101241734
```

### Options

```
  -h, --help                   help for create
      --name string            Device name (required)
      --serial-number string   Device serial number (required)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
