## devicemanager tunnel update

Update a tunnel

```
devicemanager tunnel update <tunnel-id> [flags]
```

### Options

```
  -h, --help                   help for update
      --local-address string   Local address
      --local-port int         Local port
      --name string            Tunnel name
      --proto string           Protocol (http/https/tcp)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
