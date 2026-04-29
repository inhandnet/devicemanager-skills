## devicemanager update

Update devicemanager CLI to the latest version

Check for and install newer versions of the devicemanager CLI.
By default, downloads and installs the latest release.
Use --check to only check without installing.

### Examples

```
  # Update to latest version
  devicemanager update

  # Check for updates without installing
  devicemanager update --check

  # Check for updates (JSON output, useful for scripts)
  devicemanager update --check -o json

  # Update to a specific version
  devicemanager update --version v0.3.0

  # Skip confirmation prompt (for scripts/CI)
  devicemanager update --yes
```

### Options

```
      --check            Only check for updates, don't install
      --version string   Update to a specific version (e.g. v0.3.0)
  -y, --yes              Skip confirmation prompt
  -o, --output string    Output format for --check (json)
```
