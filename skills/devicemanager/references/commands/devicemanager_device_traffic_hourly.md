## devicemanager device traffic hourly

Query hourly traffic for a device

### Examples

```
  # Last 24 hours (default)
  devicemanager device traffic hourly <device-id>

  # Custom date range (max 6 days)
  devicemanager device traffic hourly <device-id> --after 2026-04-25 --before 2026-04-27
```

### Options

```
  <device-id>       Device ID (required positional argument)
      --after string    Start date (YYYY-MM-DD)
      --before string   End date (YYYY-MM-DD, max 6 days from after)
```
