## devicemanager devicegroup create

Create a device group

```
devicemanager devicegroup create [flags]
```

### Examples

```
  devicemanager devicegroup create --name "Factory A"
  devicemanager devicegroup create --name "Line 1" --parent <group-id>
```

### Options

```
  -h, --help            help for create
      --name string     Group name (required)
      --parent string   Parent group ID
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
