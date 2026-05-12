## devicemanager system user list

List users in the organization

```
devicemanager system user list [flags]
```

### Examples

```
  # List users in current organization
  devicemanager system user list

  # List users in a specific organization
  devicemanager system user list --oid <org-id>
```

### Options

```
  -h, --help         help for list
      --oid string   Organization ID (list users of a specific org)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
