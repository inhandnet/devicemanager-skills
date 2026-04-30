## devicemanager system permission create

Create a device permission group

```
devicemanager system permission create [flags]
```

### Examples

```
  devicemanager system permission create --name "office-devices" --desc "Office routers"
```

### Options

```
      --desc string   Description
  -h, --help          help for create
      --name string   Permission group name (required)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
