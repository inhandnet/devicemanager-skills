## devicemanager system log list

List audit logs

```
devicemanager system log list [flags]
```

### Examples

```
  # List recent audit logs
  devicemanager system log list

  # Filter by date range
  devicemanager system log list --start-time 2026-04-24 --end-time 2026-04-30

  # Filter by level
  devicemanager system log list --level warning
```

### Options

```
      --cursor int          Skip N items (pagination offset)
      --end-time string     End date (YYYY-MM-DD)
  -h, --help                help for list
      --level string        Filter by level
      --limit int           Number of items per page (default 20)
      --start-time string   Start date (YYYY-MM-DD)
      --verbose int         Detail level (1-100, higher = more fields) (default 10)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
