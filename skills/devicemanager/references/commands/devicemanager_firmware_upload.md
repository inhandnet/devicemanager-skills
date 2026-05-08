## devicemanager firmware upload

Upload a firmware file

### Synopsis

Upload a firmware binary file to the platform. Returns a file ID (fid) that
is needed when creating a firmware record with 'firmware create --fid <fid>'.

```
devicemanager firmware upload <file-path> [flags]
```

### Examples

```
  # Upload firmware and note the returned file ID
  devicemanager firmware upload ./IG502-V2.0.0.rl4207.bin
```

### Options

```
  -h, --help   help for upload
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
