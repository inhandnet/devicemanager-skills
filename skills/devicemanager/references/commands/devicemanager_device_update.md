## devicemanager device update

Update a device

```
devicemanager device update <device-id> [flags]
```

### Examples

```
  # Rename a device
  devicemanager device update 5d6349d6335c8c000178a194 --name "new-name"

  # Update description
  devicemanager device update 5d6349d6335c8c000178a194 --description "office router"
```

### Options

```
      --description string   New device description
  -h, --help                 help for update
      --name string          New device name
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
