## devicemanager docs get

Fetch a specific document by path

```
devicemanager docs get <path> [flags]
```

### Examples

```
  # Fetch with full path
  devicemanager docs get ER805/troubleshooting/vpn.md

  # Fetch with --model prefix (equivalent to above)
  devicemanager docs get troubleshooting/vpn.md --model ER805
```

### Options

```
  -h, --help           help for get
      --model string   Prepend model directory to path (e.g. ER805)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
