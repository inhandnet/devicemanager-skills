## devicemanager devicegroup devices list

List devices in a group

### Examples

```
  devicemanager devicegroup devices list <group-id>
  devicemanager devicegroup devices list <group-id> --recursive --online 1
```

### Options

```
  <group-id>                  Group ID (required positional argument)
      --name string           Filter by device name
      --serial-number string  Filter by serial number
      --online string         Filter by online status (0=offline, 1=online)
      --recursive             Include devices from sub-groups
      --cursor int            Skip N items (pagination offset) (default 0)
      --limit int             Number of items per page (default 20)
      --verbose int           Detail level (1-100, higher = more fields) (default 10)
```
