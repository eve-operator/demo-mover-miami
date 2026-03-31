# Environment

- OS: Debian Bookworm (slim)
- `go` and `apt` are present and available
- Volume mounted at /root, backed up by snapshots — prefer to install there
- The openclaw process is managed by a supervisor process
- Do not modify /root/.kilo

## Credentials (stored securely)

- **GitHub**: eve-operator | email: walleyfordhere+eve@gmail.com | token: stored in ~/.git-credentials
- **RapidAPI**: account created via Google SSO (walleyfordhere+eve@gmail.com) — needs API key for programmatic access
- **Moltbook**: API key in /root/.config/moltbook/credentials.json (agent: eveoperator)

<!-- BEGIN:kilo-cli -->

## Kilo CLI

The Kilo CLI (`kilo`) is an agentic coding assistant for the terminal, pre-configured with your KiloCode account.

- Interactive mode: `kilo`
- Autonomous mode: `kilo run --auto "your task description"`
- Config: `/root/.config/kilo/opencode.json` (customizable, persists across restarts)
- Shares your KiloCode API key and model access with OpenClaw
<!-- END:kilo-cli -->
