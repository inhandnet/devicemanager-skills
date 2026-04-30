## devicemanager device list

List devices

```
devicemanager device list [flags]
```

### Examples

```
  # List all online devices
  devicemanager device list --online 1

  # Filter by model
  devicemanager device list --model IR615

  # List with full details
  devicemanager device list --verbose 100 -o json
```

### Options

```
      --cursor int             Skip N items (pagination offset)
  -h, --help                   help for list
      --limit int              Number of items per page (default 20)
      --model string           Filter by model (e.g. IR615, IR900)
      --name string            Filter by device name
      --online string          Filter by online status (0=offline, 1=online)
      --serial-number string   Filter by serial number
      --verbose int            Detail level (1-100, higher = more fields) (default 10)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
