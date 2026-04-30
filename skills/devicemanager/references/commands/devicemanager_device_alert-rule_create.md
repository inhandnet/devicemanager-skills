## devicemanager device alert-rule create

Create an alert rule

```
devicemanager device alert-rule create [flags]
```

### Examples

```
  devicemanager device alert-rule create --name "offline-alert" \
    --metric online --condition eq --threshold 0 --duration 300
```

### Options

```
      --condition string   Condition operator (required)
      --duration string    Duration in seconds
  -h, --help               help for create
      --metric string      Metric to monitor (required)
      --name string        Rule name (required)
      --threshold string   Threshold value (required)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
