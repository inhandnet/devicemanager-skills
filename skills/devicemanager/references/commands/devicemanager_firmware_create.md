## devicemanager firmware create

Create a firmware entry

```
devicemanager firmware create [flags]
```

### Examples

```
  devicemanager firmware create --fid <file-id> --name "IR615-v2.0" --version 2.0.0 --model IR615
```

### Options

```
      --desc string       Description
      --fid string        Uploaded file ID (required)
  -h, --help              help for create
      --job-timeout int   Job timeout (seconds)
      --model string      Device model (required)
      --name string       Firmware name (required)
      --version string    Firmware version (required)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
