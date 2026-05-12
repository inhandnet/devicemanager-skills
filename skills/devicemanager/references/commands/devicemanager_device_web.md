## devicemanager device web

Start remote web management for a device

```
devicemanager device web <device-id> [flags]
```

### Examples

```
  # Start remote web management
  devicemanager device web <device-id>

  # Use custom port
  devicemanager device web <device-id> --port 443 --proto https
```

### Options

```
  -h, --help            help for web
      --port int        Device web management port (default 80)
      --proto string    Protocol (http/https) (default "http")
      --server string   Ngrok server address (default "ngrok.j3r0lin.com:4443")
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
