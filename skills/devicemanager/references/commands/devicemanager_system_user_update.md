## devicemanager system user update

Update a user

```
devicemanager system user update <user-id> [flags]
```

### Options

```
  -h, --help             help for update
      --name string      New user name
      --role-id string   New role ID (use 'system role list' to find IDs)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
