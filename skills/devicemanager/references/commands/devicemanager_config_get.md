## devicemanager config get

Get configuration values

```
devicemanager config get [key] [flags]
```

### Examples

```
  # Get all config values
  devicemanager config get

  # Get specific value
  devicemanager config get ngrok-server
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
