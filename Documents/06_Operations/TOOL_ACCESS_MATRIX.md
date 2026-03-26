# TOOL_ACCESS_MATRIX.md

_Audit date: 2026-03-26_

## What Each Tool Can Do

### File Operations
| Tool | Read | Write | Execute |
|------|------|-------|---------|
| read | ✅ | ❌ | ❌ |
| write | ❌ | ✅ | ❌ |
| edit | ❌ | ✅ (surgical) | ❌ |
| exec | ✅ | ✅ | ✅ |

### External
| Tool | Scope | Auth | Risk Level |
|------|-------|------|------------|
| web_search | Web queries | Brave API key | Low |
| web_fetch | URL content | None (public) | Low |
| browser | Full browser control | Depends on profile | Medium-High |
| message | Telegram send/receive | Bot token | Medium |
| tts | Audio generation | Provider key | Low |

### Internal
| Tool | Scope | Risk Level |
|------|-------|------------|
| memory_search/get | Workspace memory files | Low |
| sessions_* | Sub-agent management | Medium |
| session_status | Status/cost info | Low |

## Pending Access (Need to Configure)

- [ ] GitHub CLI (`gh`) — needs auth
- [ ] Email — no provider configured
- [ ] Calendar — no provider configured  
- [ ] 1Password CLI — not installed
- [ ] Cloud providers — none configured
- [ ] SSH keys — not audited

## Least Privilege Notes

- Browser: prefer sandbox profile over user profile
- Exec: prefer specific commands over open-ended shells
- Message: only send to known targets
