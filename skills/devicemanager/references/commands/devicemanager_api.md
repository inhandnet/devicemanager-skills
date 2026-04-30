## devicemanager api

Make an authenticated API request

### Synopsis

Make an authenticated API request to the DM platform.

The path is appended to the current context's host URL.
Authorization header is automatically injected.

```
devicemanager api <path> [flags]
```

### Examples

```
  # GET current user
  devicemanager api /api/users/this

  # List devices with query params
  devicemanager api /api/devices -q page=0 -q limit=10

  # Output formats
  devicemanager api /api/devices -o json
  devicemanager api /api/devices -o table -c name -c online
  devicemanager api /api/devices -o yaml

  # Create device
  devicemanager api /api/devices -X POST -f name=test -f serialNumber=SN001

  # POST with JSON from stdin
  echo '{"name":"test"}' | devicemanager api /api/devices -X POST --input -

  # Custom header
  devicemanager api /api/users/this -H "Sudo: user@example.com"

  # Download a file
  devicemanager api /api/devices/DEVICE_ID/files/capture_result.pcap --output-file capture.pcap
```

### Options

```
  -c, --column stringArray   Columns to show in table output
  -f, --field stringArray    Body field (key=value), sent as JSON
  -H, --header stringArray   Additional header (Key: Value)
  -h, --help                 help for api
      --input string         Read body from file (use - for stdin)
  -X, --method string        HTTP method (default: GET)
      --output-file string   Save response body to file (for binary downloads)
  -q, --query stringArray    Query parameter (key=value)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
