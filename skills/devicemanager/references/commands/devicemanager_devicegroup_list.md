## devicemanager devicegroup list

List device groups

```
devicemanager devicegroup list [flags]
```

### Options

```
  -h, --help            help for list
      --max-depth int   Max depth of group tree (default 3)
      --parent string   Filter by parent group ID
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
