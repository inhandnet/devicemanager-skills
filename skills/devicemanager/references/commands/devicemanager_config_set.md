## devicemanager config set

Set a global configuration value

```
devicemanager config set <key> <value> [flags]
```

### Examples

```
  # Set custom ngrok server
  devicemanager config set ngrok-server my-ngrok.example.com:4443
```

### Options

```
  -h, --help   help for set
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
