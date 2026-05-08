## devicemanager system permission devicegroups remove

Remove device groups from a permission group

```
devicemanager system permission devicegroups remove <group-id> <devicegroup-id>... [flags]
```

### Examples

```
  devicemanager system permission devicegroups remove <group-id> <devicegroup-id1>
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
```
