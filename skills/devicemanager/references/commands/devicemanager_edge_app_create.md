## devicemanager edge app create

Create an edge app

```
devicemanager edge app create [flags]
```

### Examples

```
  devicemanager edge app create --name "my-app" --description "My edge app"
```

### Options

```
      --description string   App description
  -h, --help                 help for create
      --name string          App name (required)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
