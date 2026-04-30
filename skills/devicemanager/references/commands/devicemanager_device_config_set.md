## devicemanager device config set

Set device configuration

```
devicemanager device config set <device-id> [flags]
```

### Examples

```
  devicemanager device config set <device-id> --content "..."
  devicemanager device config set <device-id> --content-file config.json
```

### Options

```
      --content string        Configuration content
      --content-file string   Configuration file path
      --description string    Configuration description
  -h, --help                  help for set
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
