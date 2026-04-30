## devicemanager device traffic monthly

Query monthly traffic for a device (YYYYMM)

```
devicemanager device traffic monthly <month> <device-id> [flags]
```

### Examples

```
  devicemanager device traffic monthly 202604 <device-id>
```

### Options

```
  -h, --help   help for monthly
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
