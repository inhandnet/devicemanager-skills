## devicemanager auth login

Login via browser

### Examples

```
  # Login via browser (default) — opens DM login page
  devicemanager auth login

  # Login to global region
  devicemanager auth login --host global

  # Login with a custom domain
  devicemanager auth login --host iot.example.com
```

### Options

```
      --context string    Context name to create/update (default "default")
      --host string       Platform region: "cn", "global", or a custom domain (default "cn")
      --port int          Local callback server port (default 18920)
      --timeout duration  Timeout waiting for browser login (default 3m0s)
```
