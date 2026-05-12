## devicemanager system user create

Create a user

### Synopsis

Create a user and send an invitation email. The user sets their password via the email link.

```
devicemanager system user create [flags]
```

### Examples

```
  # Create an internal user (invitation email sent automatically)
  devicemanager system user create --name "test" --email "test@example.com"

  # Create with a specific role ID
  devicemanager system user create --name "test" --email "test@example.com" --role-id <role-id>

  # Create an external user
  devicemanager system user create --email "ext@example.com" --external
```

### Options

```
      --email string     User email (required)
      --external         Create as external user
  -h, --help             help for create
      --lang string      Invitation email language: "en" (default) or "zh"
      --name string      User name
      --role-id string   Role ID (required, use 'system role list' to find IDs)
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
