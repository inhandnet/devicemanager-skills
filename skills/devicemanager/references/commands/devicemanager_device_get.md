## devicemanager device get

Get device details

```
devicemanager device get <device-id> [flags]
```

### Examples

```
  # Get full device details
  devicemanager device get 5d6349d6335c8c000178a194 --verbose 100
```

### Options

```
  -h, --help          help for get
      --verbose int   Detail level (1-100) (default 100)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
