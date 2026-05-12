## devicemanager edge app deploy

Deploy an edge app version to devices or device groups

```
devicemanager edge app deploy <app-id> --version <version> [device-id]... [flags]
```

### Options

```
      --group strings    Device group IDs to deploy to
  -h, --help             help for deploy
      --version string   App version to deploy (required)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
