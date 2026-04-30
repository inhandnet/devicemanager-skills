## devicemanager auth impersonate

Impersonate another user (requires ROOT privilege)

```
devicemanager auth impersonate [flags]
```

### Examples

```
  # Impersonate by user ID (auto-resolves internal org)
  devicemanager auth impersonate --user 5e0956c46aa6d10001e931ea

  # Impersonate by org ID (auto-resolves org admin)
  devicemanager auth impersonate --org 5e0956c46aa6d10001e931e6

  # Impersonate with both user and org
  devicemanager auth impersonate --user <uid> --org <oid>

  # Stop impersonation and restore admin identity
  devicemanager auth impersonate --stop
```

### Options

```
  -h, --help          help for impersonate
      --org string    Organization ID
      --stop          Stop impersonation and restore admin identity
      --user string   User ID to impersonate
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
