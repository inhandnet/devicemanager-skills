## devicemanager edge version deploy

Deploy an edge app version to devices

```
devicemanager edge version deploy <app-id> <version> [flags]
```

### Options

```
      --device strings   Device IDs to deploy
      --group strings    Device group IDs to deploy
  -h, --help             help for deploy
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
