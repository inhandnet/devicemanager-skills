## devicemanager docs list

List available models or model-specific documents

```
devicemanager docs list [flags]
```

### Examples

```
  # List all available models
  devicemanager docs list

  # List documents for a specific model
  devicemanager docs list --model ER805
```

### Options

```
  -h, --help           help for list
      --model string   Show index for a specific model (e.g. ER805, IR615)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
