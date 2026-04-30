## devicemanager tunnel create

Create a tunnel

```
devicemanager tunnel create [flags]
```

### Examples

```
  devicemanager tunnel create --name ssh-tunnel --device-id <id> --proto tcp --local-address 127.0.0.1 --local-port 22
```

### Options

```
      --device-id string       Device ID (required)
  -h, --help                   help for create
      --local-address string   Local address (default "127.0.0.1")
      --local-port int         Local port (required)
      --name string            Tunnel name (required)
      --proto string           Protocol (http/https/tcp) (default "tcp")
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
