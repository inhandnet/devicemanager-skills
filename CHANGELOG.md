# Changelog

## v0.5.6 (2026-05-13)

### Bug Fixes (CLI v0.5.6 sync)

- **Auth impersonate**: Fix resolving wrong user when using org name — now resolves org name → ObjectID first; reports error on ambiguous org names
- **DRC commands**: All DRC commands now pass `oid` query parameter, fixing wrong org data after impersonation
- **DRC/firmware devices add**: Always send both `deviceIds` and `deviceGroupIds` (even as empty arrays), fixing `Service unavailable` error
- **Firmware cancel**: Simplified to `DELETE /api/job/{firmwareID}/devices/{deviceID}`
- **File upload 400**: `device import`, `firmware upload`, `edge agent upload`, `edge version upload` now pass `access_token` as query parameter instead of Authorization header
- **Device web**: Add polling for task completion instead of only checking initial response
- **Edge agent devices**: `--status` now defaults to `pending` (required by API); values corrected to lowercase

### Improvements

- **Firmware cheatsheet**: `firmware cancel/retry/job-stats/devices remove` renamed `<job-id>` → `<firmware-id>` with usage hints
- **Edge agent devices cheatsheet**: Status values corrected to lowercase, default noted
- **System user list**: Auto-applies `oid` from impersonated context
- **Command references**: Regenerated 181 docs for v0.5.6

---

## v0.5.5 (2026-05-12)

### New Features

- **Device import**: Add `device import` to cheatsheet — batch import from Excel with `--group` and `--no-overwrite`
- **Device web**: Add `device web` to cheatsheet — remote web management via ngrok
- **Edge deploy/undeploy**: Add `edge agent deploy/undeploy`, `edge app deploy/undeploy`, `edge config undeploy` to cheatsheet and edge-computing reference
- **Edge control remove**: Add `edge control remove` (uninstall app) to cheatsheet and edge-computing reference
- **Edge device status**: Add `edge device` (query device agent & apps) to cheatsheet and edge-computing reference
- **Firmware delete/cancel/retry**: Add `firmware delete`, `firmware cancel`, `firmware retry` to cheatsheet and firmware-upgrade reference
- **User list --oid**: Add `--oid` filter to `system user list` cheatsheet
- **Org list filters**: Add `--name`/`--email` to `system org list` cheatsheet

### Improvements

- **Task list**: Update cheatsheet with correct `--type` values (`config-apply`, `interactive-command`, etc.) and `--status` values (`running`, `waiting`, `failed`, `completed`)
- **DRC devices add**: Update cheatsheet to show group-only assignment support
- **Firmware devices add**: Update cheatsheet to show group-only assignment support
- **Agent devices status**: Add full status enum (`PENDING/INSTALLING/DOWNLOADING/READY/FAILED`)
- **Verbose**: Update cheatsheet — global `--verbose` (default 100), GET only
- **Edge-computing reference**: Add deploy/undeploy/remove/device workflows
- **Firmware-upgrade reference**: Add cancel/retry workflow, fix upload syntax, note timeout default
- **Command references**: Regenerated 181 docs for v0.5.5

---

## v0.5.4 (2026-05-09)

### New Features

- **Traffic stats**: Add `device traffic stats` to cheatsheet — per-device traffic with filtering and pagination
- **Online stats**: Update cheatsheet — no longer requires `--device-id`, supports `--name/--model/--online` filters

### Improvements

- **Config export**: Update cheatsheet to note file download and `--file` option
- **Command references**: Regenerated for v0.5.4

---

## v0.5.3 (2026-05-09)

### Improvements

- **Config get**: Update cheatsheet to note auto-refresh and `--skip-refresh` option
- **Traffic hourly**: Update cheatsheet to note default 2-day range
- **Traffic top**: Update cheatsheet with `YYYY-MM` format and default current month
- **Command references**: Regenerated for v0.5.3

---

## v0.5.2 (2026-05-08)

### Bug Fixes

- **Task list**: Update cheatsheet with correct parameter names (`states`/`types`/`--object-id`)
- **Command references**: Regenerated 168 docs to reflect all v0.5.2 API path, parameter, and help text fixes

---

## v0.5.1 (2026-05-08)

### Bug Fixes

- **System log**: Update cheatsheet to note default 7-day range
- **Signal**: Update cheatsheet to note `--before` defaults to now
- **Command references**: Regenerated to reflect devicegroup/tunnel list flag fixes

---

## v0.5.0 (2026-05-07)

### New Features

- **Permission**: Restructure `users/devices/devicegroups` as subcommand groups with `list/add/remove` for managing group members
- **Org update**: `--country` now uses ISO 3166-1 alpha-2 code (e.g. CN, US)
- **Command references**: Updated to 168 auto-generated command docs

---

## v0.4.0 (2026-05-07)

### New Features

- **Device**: Add `models`, `stats`, `count online/total`, `traffic top`, `config export` command references and cheatsheet
- **Firmware**: Add `get`, `job-stats` command references and cheatsheet
- **System**: Add `role list`, `org list`, `permission devicegroups`, `permission unassigned-users` command references and cheatsheet
- **Command references**: Updated to 159 auto-generated command docs
- **Command references**: Updated to 159 auto-generated command docs

---

## v0.3.0 (2026-05-07)

### Breaking Changes

- **Alert rule fields**: Create/update commands now use `--alert-type`/`--for-device-type`/`--notify-users`/`--notify-types`/`--webhook-url` instead of old `--metric`/`--condition`/`--threshold`
- **User create**: No longer requires `--password`; uses invitation email flow. Added `--role-id`, `--external`, `--lang`
- **Auth impersonate**: `--org` is now required; `--user` is optional and must be combined with `--org`
- **Default region**: `--host` default changed from `cn` to `global`

### Improvements

- **SKILL.md**: Update alert-rule, user, permission, org, device cheatsheet to match new CLI flags
- **Command references**: Regenerated to 145 command docs

---

## v0.2.2 (2026-05-06)

### New Features

- **Device documentation**: Add `docs list/get/search` command references for browsing [model-reference](https://github.com/inhandnet/model-reference) repo
- **SKILL.md**: Add device docs cheatsheet section and rule 13 (query device model → search docs → read before answering)
- **SKILL.md**: Add reference loading entries for device config and troubleshooting scenarios

### Improvements

- **Command references**: Updated to 145 auto-generated command docs

---

## v0.2.1 (2026-05-06)

### New Features

- **Impersonate & org switching**: Add `auth impersonate`, `auth orgs`, `auth switch-org` command references

### Improvements

- **Command references**: Updated to 141 auto-generated command docs
- **SKILL.md**: Add impersonate, orgs, switch-org to auth cheatsheet

---

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
