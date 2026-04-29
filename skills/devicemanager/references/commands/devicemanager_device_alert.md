## devicemanager device alert

List device alerts

### Examples

```
  devicemanager device alert
  devicemanager device alert --device-name "router-1" --state unconfirmed
  devicemanager device alert --start-time 2024-01-01T00:00:00Z --end-time 2024-01-31T23:59:59Z
```

### Options

```
      --device-name string  Filter by device name
      --rule-name string    Filter by rule name
      --start-time string   Filter by start time (ISO8601)
      --end-time string     Filter by end time (ISO8601)
      --state string        Filter by state (confirmed/unconfirmed)
      --cursor int          Skip N items (pagination offset) (default 0)
      --limit int           Number of items per page (default 20)
      --verbose int         Detail level (1-100, higher = more fields) (default 10)
```

Aliases: `alerts`
