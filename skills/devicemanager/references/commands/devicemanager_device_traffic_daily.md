## devicemanager device traffic daily

Query daily traffic for a device (YYYYMM)

```
devicemanager device traffic daily <month> <device-id> [flags]
```

### Examples

```
  devicemanager device traffic daily 202604 <device-id>
```

### Options

```
  -h, --help   help for daily
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
