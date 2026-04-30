# Changelog

## v0.2.0 (2026-04-30)

### New Features

- **Device update/delete**: Add `device update` and `device delete` commands
- **Alert rules**: Full CRUD for alert rules (`alert-rule list/get/create/update/delete/enable/disable`)
- **Alert acknowledge**: Add `device alert-ack` to confirm alerts
- **Online statistics**: Add `device online-stats` for device online rate and duration analysis
- **Impersonate & org switching**: Add `auth impersonate`, `auth orgs`, `auth switch-org` commands
- **Device diagnostics**: Add `device online-events` (online/offline event timeline), `device register-events` (registration history), and `edge app logs` (edge app runtime logs) for troubleshooting
- **Task management**: Unified task view with `task list/cancel/restart`
- **System management**: New `system` command group:
  - `system user list/get/create/update/delete` — user management
  - `system permission list/get/create/update/delete/users/devices` — device permission groups
  - `system org get/update` — organization info
  - `system log list` — audit log query

### Improvements

- **Command references**: Updated from 99 to 141 auto-generated command docs
- **SKILL.md**: Update install section to reference `INSTALL.md` from devicemanager-cli instead of `go install`, enabling fully automated CLI installation by AI assistants
- **SKILL.md**: Added command cheatsheet sections for alert rules, tasks, system management; updated reference loading table

---

## v0.1.2 (2026-04-29)

### Improvements

- **Command references**: Add `-y/--yes` skip confirmation prompt flag to all 11 destructive commands (delete, remove, kick, reboot)

---

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
