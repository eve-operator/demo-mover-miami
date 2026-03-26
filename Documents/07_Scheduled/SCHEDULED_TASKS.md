# SCHEDULED_TASKS.md

## 12-Hour Review Cycle

| Cycle | Next Run | Status |
|-------|----------|--------|
| Morning review | Start of each day UTC | Via HEARTBEAT.md |
| 12-hour review | Every 12 hours | Via HEARTBEAT.md |

## Cron Jobs

_(Configure via openclaw when ready)_

| Job | Schedule | Purpose | Status |
|-----|----------|---------|--------|
| 12-hour report | Every 12h | Generate status report | ⬜ Via heartbeat |
| Memory maintenance | Weekly | Daily logs → MEMORY.md | ⬜ Pending |
| Secrets re-audit | Monthly | Scan for new plaintext | ⬜ Pending |

## Self-Maintenance Rotation (20% Budget)

Rotated each heartbeat:
1. Secrets scan
2. Git hygiene
3. Tool access verification
4. Memory maintenance
5. Cost check
6. Workspace cleanliness
