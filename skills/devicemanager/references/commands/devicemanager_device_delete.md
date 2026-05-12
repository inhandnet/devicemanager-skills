## devicemanager device delete

Delete a device

### Synopsis

Permanently remove a device from the platform. This action cannot be undone.

```
devicemanager device delete <device-id> [flags]
```

### Examples

```
  devicemanager device delete 5d6349d6335c8c000178a194
  devicemanager device delete 5d6349d6335c8c000178a194 -y  # Skip confirmation
```

### Options

```
  -h, --help   help for delete
  -y, --yes    Skip confirmation prompt
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
