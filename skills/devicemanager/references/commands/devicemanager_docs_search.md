## devicemanager docs search

Search documents by keyword in model index

```
devicemanager docs search <keyword> [flags]
```

### Examples

```
  # Search across a model's documents
  devicemanager docs search VPN --model ER805

  # Search root index (lists matching models)
  devicemanager docs search ER805

  # Search multiple keywords (quote them)
  devicemanager docs search "port forwarding" --model IR615
```

### Options

```
  -h, --help           help for search
      --model string   Search within a model's index (e.g. ER805, IR615)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
```
