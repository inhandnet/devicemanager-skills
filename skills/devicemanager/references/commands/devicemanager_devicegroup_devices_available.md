## devicemanager devicegroup devices available

List devices that can be added to a group

### Examples

```
  devicemanager devicegroup devices available <group-id>
  devicemanager devicegroup devices available <group-id> --name "router"
```

### Options

```
  <group-id>                  Group ID (required positional argument)
      --name string           Filter by device name
      --serial-number string  Filter by serial number
      --cursor int            Skip N items (pagination offset) (default 0)
      --limit int             Number of items per page (default 20)
      --verbose int           Detail level (1-100, higher = more fields) (default 10)
```
