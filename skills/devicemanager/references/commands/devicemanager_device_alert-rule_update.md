## devicemanager device alert-rule update

Update an alert rule

```
devicemanager device alert-rule update <rule-id> [flags]
```

### Options

```
      --alert-time-end string      Alert time range end (HH:MM, e.g. 18:00)
      --alert-time-start string    Alert time range start (HH:MM, e.g. 08:00)
      --for-device-type string     Target scope: ALL, DEVICE_GROUP, or DEVICE
      --for-device-value strings   Target device/group IDs (comma-separated)
  -h, --help                       help for update
      --name string                New rule name
      --notify-delay int           Delay in minutes before alerting
      --notify-types strings       Notification types: email, sms, webhook (comma-separated)
      --notify-users strings       User IDs to notify (comma-separated)
      --webhook-secret string      Webhook secret
      --webhook-url string         Webhook URL
```

### Options inherited from parent commands

```
      --context string   Override active context (env: DEVICEMANAGER_CONTEXT)
      --debug            Enable debug output (env: DEVICEMANAGER_DEBUG)
      --jq string        Filter JSON output using a jq expression (implies -o json)
  -o, --output string    Output format: json, table, yaml (default: table for TTY, json otherwise)
      --verbose int      API response detail level (1-100, higher = more fields) (default 100)
```
