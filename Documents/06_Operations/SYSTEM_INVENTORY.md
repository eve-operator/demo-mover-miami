# SYSTEM_INVENTORY.md

## Environment

- **OS:** Debian Bookworm (slim)
- **Runtime:** Node v22.22.1 on Linux 6.12.47-fly (x64)
- **Host:** 90803e3df31368
- **OpenClaw:** Managed by supervisor process
- **Agent model:** kilocode/kilo-auto/free (default)
- **Channel:** Telegram (direct chat with Jason)

## Installed Tools

| Tool | Available | Notes |
|------|-----------|-------|
| git | ✅ | Workspace is a git repo |
| go | ✅ | In PATH |
| apt | ✅ | Package manager |
| node/npm | ✅ | v22.22.1 |
| openclaw | ✅ | CLI available |
| kilo | ✅ | Agentic coding assistant |
| web_search | ✅ | Brave Search API |
| web_fetch | ✅ | URL content extraction |
| browser | ✅ | Sandbox + host profiles |
| exec | ✅ | Shell command execution |
| message | ✅ | Telegram channel |
| tts | ✅ | Text-to-speech |
| memory_search/get | ✅ | Semantic memory search |
| sessions_spawn | ✅ | Sub-agents / ACP |
| cron (scheduled) | TBD | Need to configure |

## Capabilities

- Read/write/edit files in workspace
- Execute shell commands
- Web search and fetch
- Browser automation (sandbox + user profiles)
- Telegram messaging with inline buttons
- TTS audio generation
- Sub-agent spawning
- Session management
- Memory (semantic search + file-based)

## Limitations

- No email access configured
- No calendar access configured
- No GitHub CLI auth configured (needs verification)
- No cloud provider access
- No VPN/SSH tunneling configured
- Model: free tier (may have rate limits)

## File System

- Workspace: `/root/.openclaw/workspace/`
- Backed by volume snapshots (good for recovery)
- Do NOT modify `/root/.kilo`
