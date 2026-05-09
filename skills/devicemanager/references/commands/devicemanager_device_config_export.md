## devicemanager device config export

Export device configuration to a file

```
devicemanager device config export <device-id> [flags]
```

### Examples

```
  # Export to current directory (filename from server)
  devicemanager device config export <device-id>

  # Export to a specific path
  devicemanager device config export <device-id> --file ./my-config.dat
```

### Options

```
  -f, --file string   Output file path (default: server filename in current directory)
  -h, --help          help for export
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
