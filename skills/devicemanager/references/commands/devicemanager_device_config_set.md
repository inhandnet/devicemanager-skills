## devicemanager device config set

Set device configuration

### Examples

```
  devicemanager device config set <device-id> --content "..."
  devicemanager device config set <device-id> --content-file config.json
```

### Options

```
      --content string       Configuration content
      --content-file string  Configuration file path
      --description string   Configuration description
```

Note: Either `--content` or `--content-file` is required.
