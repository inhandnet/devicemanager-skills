## devicemanager drc create

Create a DRC template

```
devicemanager drc create [flags]
```

### Examples

```
  devicemanager drc create --name "IR615-default" --model IR615 --content "..."
```

### Options

```
      --content string        Template content (required)
      --content-type string   Content type
      --desc string           Description
  -h, --help                  help for create
      --model string          Device model (required)
      --name string           Template name (required)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
