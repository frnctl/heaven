# Heaven

✦ **HEAVEN · Sync the universe. One word. Peace forever.** ✦

Heaven is a single-command CLI utility to automatically synchronize, clone, and deploy all your GitHub repositories into your local workspace. It finds your repos on GitHub, clones any that are missing, and synchronizes (pulls/commits/pushes) the ones you already have.

## Installation

You can install `heaven` globally by putting it in a directory on your `$PATH` (e.g. `~/.local/bin`):

```bash
cp heaven ~/.local/bin/heaven
chmod +x ~/.local/bin/heaven
```

## Usage

Sync all your repositories:
```bash
heaven
```

Preview changes without applying them (dry-run):
```bash
heaven --preview
```

## Configuration

You can configure `heaven` using environment variables:

- `HEAVEN_BASE_DIR`: Where to clone/sync the repositories (default: `$HOME`)
- `HEAVEN_GH_USER`: The GitHub user or organization to fetch repositories from (default: `frnctl` or your username)

## Features
- **Smart Synchronization**: Merges, pulls, and pushes across all repositories securely.
- **Dry-run (preview)**: Check what changes will be applied before executing them.
- **Sensitive files guard**: Automatically blocks sensitive files from being committed.
- **Host-aware deployment**: If a `.kimea.conf` config is present, heaven handles local or remote deployment via SSH after syncing.
