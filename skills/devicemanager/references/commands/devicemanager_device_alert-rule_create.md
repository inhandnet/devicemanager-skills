## devicemanager device alert-rule create

Create an alert rule

```
devicemanager device alert-rule create [flags]
```

### Examples

```
  # Create an offline alert for all devices
  devicemanager device alert-rule create --name "offline-alert" --alert-type offline

  # Create an alert for specific devices with email notification
  devicemanager device alert-rule create --name "offline-alert" --alert-type offline \
    --for-device-type DEVICE --for-device-value id1,id2 \
    --notify-users uid1,uid2 --notify-types email

  # Create with webhook notification
  devicemanager device alert-rule create --name "traffic-alert" \
    --alert-type daily_traffic_excess \
    --notify-types webhook --webhook-url https://example.com/hook
```

### Options

```
      --alert-type string          Alert type: online, offline, hourly_traffic_excess, daily_traffic_excess, monthly_traffic_excess, sim_switch, link_backup, link_change, power_switch, power_fault, power_recovery (required)
      --for-device-type string     Target scope: ALL, DEVICE_GROUP, or DEVICE (default "ALL")
      --for-device-value strings   Target device/group IDs (comma-separated)
  -h, --help                       help for create
      --locale string              Notification language: "en" or "zh" (default "en")
      --name string                Rule name (required)
      --notify-delay int           Delay in minutes before alerting (for online/offline)
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
```
