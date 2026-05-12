## devicemanager system permission devices remove

Remove devices from a permission group

```
devicemanager system permission devices remove <group-id> <device-id>... [flags]
```

### Examples

```
  devicemanager system permission devices remove <group-id> <device-id1> <device-id2>
```

### Options

```
  -h, --help   help for remove
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
