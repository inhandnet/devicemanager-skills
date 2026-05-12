## devicemanager docs

Browse device model reference documentation

### Synopsis

Browse device-side documentation for configuration and troubleshooting.

Documents are organized by device model in a public GitHub repository.
Each model has its own index.md describing available documents.

Reading flow: index.md (root) → <model>/index.md → specific document.

Override the default repo with DEVICEMANAGER_DOCS_REPO environment variable.

### Options

```
  -h, --help   help for docs
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
