## devicemanager task list

List tasks

```
devicemanager task list [flags]
```

### Examples

```
  # List all running tasks
  devicemanager task list --status running

  # List failed tasks
  devicemanager task list --status failed

  # Filter by type
  devicemanager task list --type firmware_upgrade
```

### Options

```
      --cursor int           Skip N items (pagination offset)
      --device-name string   Filter by device name
  -h, --help                 help for list
      --limit int            Number of items per page (default 20)
      --status string        Filter by status (running/waiting/failed/completed)
      --type string          Filter by task type
      --verbose int          Detail level (1-100, higher = more fields) (default 10)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
