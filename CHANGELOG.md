# Changelog

## v0.1.1 (2026-04-29)

### Improvements

- **Traffic commands**: Add `devicemanager device traffic hourly` command reference; update `traffic monthly` to positional arg style (remove `--device` flag)
- **Traffic analysis guide**: Add hourly traffic section and hour-level troubleshooting guidance
- **SKILL.md**: Update traffic command cheatsheet and version to 0.1.1

---

## v0.1.0 (2026-04-29)

### New Features

- **Main skill definition** (`SKILL.md`) — "DM 管家" persona with full command cheatsheet, operational rules, safety rules, and context-aware reference loading
- **98 command reference docs** — auto-generated from [devicemanager-cli](https://github.com/inhandnet/devicemanager-cli), covering all subcommands with flags, examples, and descriptions

### Reference Guides

- **Diagnostics** — device offline troubleshooting workflow (status check → signal → alerts → config → reboot)
- **Signal analysis** — cellular signal metrics interpretation (RSSI/RSRP/SINR/RSRQ) with quality thresholds
- **Edge computing** — engine/app/version/config management and deployment workflows
- **DRC templates** — batch configuration deployment via Device Remote Configuration
- **Device config** — single-device config get/set workflow with safety guidelines
- **Tunnels** — remote tunnel creation, connection, and port forwarding scenarios
- **Firmware upgrade** — single and batch OTA upgrade workflows with safety checks
- **Traffic analysis** — monthly/daily traffic statistics and anomaly investigation
