## devicemanager system permission devices add

Add devices to a permission group

```
devicemanager system permission devices add <group-id> <device-id>... [flags]
```

### Examples

```
  devicemanager system permission devices add <group-id> <device-id1> <device-id2>
```

### Options

```
  -h, --help   help for add
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
