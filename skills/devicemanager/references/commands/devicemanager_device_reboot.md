## devicemanager device reboot

Reboot a device remotely

### Synopsis

Send a reboot command to a device. The device must be online. It will go offline briefly and reconnect.

```
devicemanager device reboot <device-id> [flags]
```

### Examples

```
  devicemanager device reboot 5d6349d6335c8c000178a194
  devicemanager device reboot 5d6349d6335c8c000178a194 --timeout 30000  # 30 second timeout
```

### Options

```
  -h, --help          help for reboot
      --timeout int   Timeout in milliseconds (default 15000ms = 15s) (default 15000)
  -y, --yes           Skip confirmation prompt
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
