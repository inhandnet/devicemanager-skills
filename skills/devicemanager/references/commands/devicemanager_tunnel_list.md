## devicemanager tunnel list

List tunnels

```
devicemanager tunnel list [flags]
```

### Options

```
      --cursor int         Skip N items (pagination offset)
      --device-id string   Filter by device ID
  -h, --help               help for list
      --limit int          Number of items per page (default 20)
      --name string        Filter by tunnel name
      --verbose int        Detail level (1-100, higher = more fields) (default 10)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
