## devicemanager devicegroup devices available

List devices that can be added to a group

```
devicemanager devicegroup devices available <group-id> [flags]
```

### Options

```
      --cursor int             Skip N items (pagination offset)
  -h, --help                   help for available
      --limit int              Number of items per page (default 20)
      --name string            Filter by device name
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
