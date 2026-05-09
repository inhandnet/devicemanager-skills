## devicemanager device traffic top

Show top devices by monthly traffic

```
devicemanager device traffic top [flags]
```

### Examples

```
  devicemanager device traffic top --date 2026-04-01 --limit 10
```

### Options

```
      --date string    Date in YYYY-MM-DD format (e.g. 2026-04-01)
  -h, --help           help for top
      --limit string   Number of top devices to return (default 10) (default "10")
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
