## devicemanager device alert

List device alerts

```
devicemanager device alert [flags]
```

### Options

```
      --cursor int           Skip N items (pagination offset)
      --device-name string   Filter by device name
      --end-time string      End time exclusive (YYYY-MM-DD or unix timestamp)
  -h, --help                 help for alert
      --limit int            Number of items per page (default 20)
      --rule-name string     Filter by rule name
      --start-time string    Start time inclusive (YYYY-MM-DD or unix timestamp)
      --state string         Filter by state (confirmed/unconfirmed)
      --verbose int          Detail level (1-100, higher = more fields) (default 10)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
