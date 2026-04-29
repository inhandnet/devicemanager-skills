## devicemanager firmware devices list

List devices in a firmware upgrade job

### Examples

```
  devicemanager firmware devices list <firmware-id>
  devicemanager firmware devices list <firmware-id> --status running
```

### Options

```
  <firmware-id>               Firmware ID (required positional argument)
      --name string           Filter by device name
      --serial-number string  Filter by serial number
      --status string         Filter by status
      --cursor int            Skip N items (pagination offset) (default 0)
      --limit int             Number of items per page (default 20)
      --verbose int           Detail level (1-100, higher = more fields) (default 10)
```
