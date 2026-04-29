## devicemanager device list

List devices

### Examples

```
  # List all online devices
  devicemanager device list --online 1

  # Filter by model
  devicemanager device list --model IR615

  # List with full details
  devicemanager device list --verbose 100 -o json
```

### Options

```
      --name string           Filter by device name
      --model string          Filter by model (e.g. IR615, IR900)
      --online string         Filter by online status (0=offline, 1=online)
      --serial-number string  Filter by serial number
      --cursor int            Skip N items (pagination offset) (default 0)
      --limit int             Number of items per page (default 20)
      --verbose int           Detail level (1-100, higher = more fields) (default 10)
```

Aliases: `ls`
