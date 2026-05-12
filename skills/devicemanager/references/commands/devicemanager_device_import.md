## devicemanager device import

Batch import devices from an Excel file

```
devicemanager device import <file-path> [flags]
```

### Examples

```
  # Import devices from Excel
  devicemanager device import devices.xlsx

  # Import and assign to a device group
  devicemanager device import devices.xlsx --group <group-id>

  # Import without overwriting existing devices
  devicemanager device import devices.xlsx --no-overwrite
```

### Options

```
      --group string   Device group ID to assign imported devices to
  -h, --help           help for import
      --no-overwrite   Do not overwrite existing devices
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
