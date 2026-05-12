## devicemanager task list

List tasks

```
devicemanager task list [flags]
```

### Examples

```
  # List running tasks
  devicemanager task list --status running

  # List waiting tasks
  devicemanager task list --status waiting

  # List failed tasks
  devicemanager task list --status failed

  # List completed tasks
  devicemanager task list --status completed

  # Filter by type
  devicemanager task list --type config-apply
  devicemanager task list --type interactive-command
```

### Options

```
      --cursor int         Skip N items (pagination offset)
  -h, --help               help for list
      --limit int          Number of items per page (default 20)
      --object-id string   Filter by device ID
      --status string      Filter by status: running, waiting, failed, completed
      --type string        Filter by type: config-apply, interactive-command, fetch-config, import-firmware, vpn-channel, vpn-link-order, token-cleanup, traffic-stats, idle-notice, remote-web
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
