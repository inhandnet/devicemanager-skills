Agent skills for managing InHand Networks [Device Manager](https://iot.inhand.com.cn) platform via the `devicemanager` CLI.

These skills follow the [Agent Skills specification](https://agentskills.io/specification) so they can be used by any skills-compatible agent, including Claude Code and Codex CLI.

## What can it do?

Once installed, talk to your AI agent in natural language to manage your Device Manager platform — no need to memorize CLI commands.

- **Device monitoring** — check device status, find offline devices, view signal quality, connected clients, traffic statistics
- **Remote diagnostics** — signal analysis (RSSI/SINR/RSRP), remote reboot, force disconnect
- **Configuration** — read/push device config, DRC templates for batch config deployment
- **Device groups** — create and manage groups, batch add/remove devices
- **Remote tunnels** — create tunnels, connect/disconnect, port forwarding to device services
- **Edge computing** — manage edge engines, applications, versions, configs, remote start/stop/restart
- **Firmware upgrades** — check available firmware, single/batch OTA upgrades, track progress
- **Alerts** — view device alerts, filter by state

## Prerequisites

- A [Device Manager](https://iot.inhand.com.cn) account

> [!NOTE]
> The [`devicemanager` CLI](https://github.com/inhandnet/devicemanager-cli) is required but you don't need to install it beforehand — the skill will guide Claude through the CLI installation and login automatically on first use. You can also [install it manually](https://github.com/inhandnet/devicemanager-cli) if you prefer.

## Installation

### Claude Code Plugin

Works on all Claude Code platforms — CLI, Desktop App, Web ([claude.ai/code](https://claude.ai/code)), and IDE extensions (VS Code, JetBrains).

1. **Add the marketplace** (only needed once):

   ```
   /plugin marketplace add inhandnet/devicemanager-skills
   ```

2. **Install the plugin**:

   ```
   /plugin install devicemanager@devicemanager-skills
   ```

3. **Activate** — start a new session for the plugin to take effect:
   - **CLI**: exit and re-run `claude`
   - **Desktop App / Web**: open a new conversation
   - **IDE extensions**: restart the Claude Code panel

4. **Verify** — the plugin is loaded when you see `devicemanager` listed in `/plugin > Installed`.

> [!TIP]
> **Desktop App**: click the **+** button next to the prompt box → **Plugins** → **Add plugin** to browse and install from the plugin manager UI.

> [!TIP]
> **Interactive browser (CLI / IDE)**: run `/plugin`, go to the **Discover** tab, find **devicemanager**, and select your preferred installation scope (User / Project / Local).

> [!TIP]
> **Terminal commands** (outside the REPL):
> ```bash
> claude plugin marketplace add inhandnet/devicemanager-skills
> claude plugin install devicemanager@devicemanager-skills
> ```
> The plugin will be active on the next Claude Code session.

#### Install for your team

To share the plugin with all project collaborators, install with **project scope**:

In the REPL, run `/plugin`, go to **Discover**, select **devicemanager**, and choose **Project** scope. This adds the marketplace and plugin to `.claude/settings.json`, so teammates get it automatically when they trust the project folder.

#### Update

```
/plugin update devicemanager@devicemanager-skills
```

#### Uninstall

```
/plugin uninstall devicemanager@devicemanager-skills
```

### Codex CLI

Copy the `skills/devicemanager` directory into one of the [Codex skills directories](https://developers.openai.com/codex/skills):

```bash
# User-level (available in all projects)
cp -r skills/devicemanager ~/.agents/skills/

# Or project-level (shared with team via git)
cp -r skills/devicemanager .agents/skills/
```

### Load without installing (session only)

If you have a local clone of this repo, you can load it into Claude Code for a single session:

```bash
claude --plugin-dir /path/to/devicemanager-skills
```

## Usage

The skill supports both English and Chinese. In most cases, just describe what you need — Claude automatically activates the skill when it detects requests related to:

- Device management (list, status, offline troubleshooting)
- Signal analysis, remote reboot, force disconnect
- Configuration, DRC templates, firmware upgrades
- Device groups, remote tunnels
- Edge computing (engines, apps, versions, deployment)

```
You:    Show me all offline devices
Claude: [Automatically loads the devicemanager skill, lists offline devices]

You:    What's the signal quality of device GR543210?
Claude: [Queries signal history and analyzes RSSI/SINR/RSRP]

You:    Deploy edge app v2.0 to the "East Region" group
Claude: [Deploys the specified version to all devices in the group]
```

> [!TIP]
> **How to tell the skill is active:**
> - **CLI / IDE**: look for the loading indicator in the output:
>   ```
>   ⏺ Skill(devicemanager:devicemanager)
>     ⎿  Successfully loaded skill
>   ```
> - **Desktop App / Web**: the skill name appears highlighted in the prompt area when invoked, or Claude starts running `devicemanager` commands in its response.

You can also invoke it explicitly — type `/` in the prompt box to browse available skills, or type `/devicemanager` directly:

```
/devicemanager List all offline devices
/devicemanager Check signal quality for device GR543210
/devicemanager Create a remote tunnel to device IR915001
/devicemanager Schedule a firmware upgrade for all IR915 devices
/devicemanager Add these devices to the "East Region" group
/devicemanager Deploy edge config to device group
```

## Troubleshooting

### "devicemanager: command not found"

The `devicemanager` CLI is not installed. Follow the installation instructions at [devicemanager-cli](https://github.com/inhandnet/devicemanager-cli).

### "unauthorized" or "401" errors

Your CLI session has expired. Run `devicemanager auth login` to re-authenticate.

### Plugin skills not appearing after installation

1. Run `/reload-plugins` to reload all plugins
2. Check `/plugin > Errors` for any loading errors
3. If the issue persists, try `claude plugin uninstall devicemanager@devicemanager-skills` and reinstall

## Skills

| Skill | Description |
|-------|-------------|
| [devicemanager](skills/devicemanager) | Manage Device Manager platform resources — device monitoring, remote diagnostics, configuration, DRC templates, device groups, remote tunnels, edge computing, firmware upgrades, and alerts |
