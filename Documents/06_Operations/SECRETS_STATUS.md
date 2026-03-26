# SECRETS_STATUS.md - Credential & Secrets Audit

_Audit date: 2026-03-26 (updated)_

## Active Credentials

| # | What | Where | Risk | Status |
|---|------|-------|------|--------|
| 1 | KILOCODE_API_KEY | Env var | ✅ Safe | Active |
| 2 | OPENCLAW_GATEWAY_TOKEN | Env var | ✅ Safe | Active |
| 3 | KILO_API_KEY | Env var | ✅ Safe | Active |
| 4 | REQUIRE_PROXY_TOKEN | Env var | ✅ Safe | Active |
| 5 | Eve Gmail App Password | Needed in env | ⬜ Pending | Not yet set as env var |
| 6 | Eve Gmail address | walleyfordhere+eve@gmail.com | ✅ Non-sensitive | Active |

## Recent Changes

- **2026-03-26:** Gmail IMAP/SMTP access established via App Password
- App Password format verified working (Google App Password, not account password)
- 2FA enabled on walleyfordhere@gmail.com (confirmed via inbox email)

## Plaintext Secrets Found

**None in files.** Credentials passed via chat only — need to migrate to env vars.

## Rules

- All secrets in environment variables ✅
- No plaintext in files, notes, logs
- App Passwords are revocable from Google Account settings
- Audit monthly or on new integrations

## Next Audit

Scheduled: 2026-04-26 (monthly cadence)
