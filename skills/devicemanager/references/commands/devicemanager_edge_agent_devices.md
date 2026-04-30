## devicemanager edge agent devices

List devices deployed with an edge agent

```
devicemanager edge agent devices <agent-id> [flags]
```

### Options

```
  -h, --help            help for devices
      --status string   Filter by status (INSTALLING/DOWNLOADING/READY/FAILED)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
