## devicemanager system user create

Create a user

```
devicemanager system user create [flags]
```

### Examples

```
  devicemanager system user create --name "test" --email "test@example.com" \
    --password "123456" --role "device_monitor"
```

### Options

```
      --email string      User email (required)
  -h, --help              help for create
      --name string       User name (required)
      --password string   User password (required)
      --role string       Role name
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
