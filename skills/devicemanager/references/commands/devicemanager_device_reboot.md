## devicemanager device reboot

Reboot a device

```
devicemanager device reboot <device-id> [flags]
```

### Options

```
  -h, --help          help for reboot
      --timeout int   Timeout in milliseconds (default 15000)
  -y, --yes           Skip confirmation prompt
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
