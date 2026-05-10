# Heaven AI - Setup Instructions for Gemini

When working with this repository on a new machine (Mac, Linux, or VPS), you MUST ensure the environment is fully authenticated to use the Oracle AI features.

## Authentication Steps
If the user requests to set up or run `heaven` with AI capabilities, perform the following verifications:

1. **Check GitHub CLI (`gh`)**: Ensure `gh` is installed.
2. **Authentication with AI Scopes**: The CLI must be authenticated with the `copilot` scope to access the GitHub Models API.
   - Command to run: `gh auth login -s "copilot" --web` (For headless servers, instruct the user to complete the device flow on their local browser).
3. **Install GitHub Models Extension**: The script relies on the official extension.
   - Command to run: `gh extension install github/gh-models`

## Global Installation
To install the script globally so the user can just type `heaven`:
```bash
mkdir -p ~/.local/bin
cp heaven ~/.local/bin/heaven
chmod +x ~/.local/bin/heaven
```

**Note**: Do not block normal syncs if the user refuses AI authentication; the script gracefully falls back to a standard sync mode.