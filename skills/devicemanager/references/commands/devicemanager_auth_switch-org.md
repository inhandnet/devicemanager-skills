## devicemanager auth switch-org

Switch to a different organization

```
devicemanager auth switch-org <org-id> [flags]
```

### Examples

```
  # List your organizations first
  devicemanager auth orgs

  # Switch to another org
  devicemanager auth switch-org 5e0956c46aa6d10001e931e6
```

### Options

```
  -h, --help   help for switch-org
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
