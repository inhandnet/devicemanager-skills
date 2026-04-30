## devicemanager edge app logs

View edge app runtime logs on a device

```
devicemanager edge app logs <device-id> <app-name> [flags]
```

### Examples

```
  # View logs for app "data-collector" on a device
  devicemanager edge app logs 639acc6e078a3d0001be2963 data-collector
```

### Options

```
  -h, --help   help for logs
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
