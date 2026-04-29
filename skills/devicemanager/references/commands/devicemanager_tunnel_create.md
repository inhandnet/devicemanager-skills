## devicemanager tunnel create

Create a tunnel

### Examples

```
  devicemanager tunnel create --name ssh-tunnel --device-id <id> --proto tcp --local-address 127.0.0.1 --local-port 22
```

### Options

```
      --name string           Tunnel name (required)
      --device-id string      Device ID (required)
      --proto string          Protocol (http/https/tcp) (default "tcp")
      --local-address string  Local address (default "127.0.0.1")
      --local-port int        Local port (required)
```
