## devicemanager

Device Manager Platform CLI

### Examples

```
  # Show version
  devicemanager version

  # Login to platform
  devicemanager auth login

  # List devices
  devicemanager device list
```

### Options

```
  -o, --output string    Output format: json, table, yaml (default "json")
      --jq string        Filter JSON output using a jq expression (implies -o json)
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
```
