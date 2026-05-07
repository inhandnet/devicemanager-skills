## devicemanager device traffic top

Show top devices by monthly traffic

```
devicemanager device traffic top [flags]
```

### Examples

```
  devicemanager device traffic top --month 202604
  devicemanager device traffic top --month 202604 --limit 10
```

### Options

```
  -h, --help           help for top
      --limit string   Number of top devices to return
      --month string   Month in YYYYMM format (e.g. 202604)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
