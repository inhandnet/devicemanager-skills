## devicemanager api

Make an authenticated API request

Make an authenticated API request to the DM platform.
The path is appended to the current context's host URL.
Authorization header is automatically injected.

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
  <path>                       API path (required positional argument)
  -X, --method string          HTTP method (default: GET)
  -q, --query stringArray      Query parameter (key=value)
  -f, --field stringArray      Body field (key=value), sent as JSON
  -H, --header stringArray     Additional header (Key: Value)
      --input string           Read body from file (use - for stdin)
      --output-file string     Save response body to file (for binary downloads)
  -c, --column stringArray     Columns to show in table output
```
