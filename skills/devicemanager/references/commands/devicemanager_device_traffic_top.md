## devicemanager device traffic top

Show top devices by monthly traffic

```
devicemanager device traffic top [flags]
```

### Examples

```
  # Current month
  devicemanager device traffic top

  # Specific month
  devicemanager device traffic top --date 2026-04
  devicemanager device traffic top --date 2026-04 --limit 20
```

### Options

```
      --date string    Month (YYYY-MM, e.g. 2026-04)
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
