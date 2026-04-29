## devicemanager drc devices list

List devices assigned to a DRC template

### Examples

```
  devicemanager drc devices list <template-id>
  devicemanager drc devices list <template-id> --status running
```

### Options

```
  <template-id>               Template ID (required positional argument)
      --name string           Filter by device name
      --serial-number string  Filter by serial number
      --status string         Filter by status (pending/running/failed/completed)
      --cursor int            Skip N items (pagination offset) (default 0)
      --limit int             Number of items per page (default 20)
      --verbose int           Detail level (1-100, higher = more fields) (default 10)
```
