# HEARTBEAT.md

## 12-Hour Review Cycle

When this heartbeat fires:

1. Read `Documents/03_Objectives/PRIMARY_OBJECTIVES.md` — are priorities still correct?
2. Read `Documents/03_Objectives/PRIORITY_QUEUE.md` — what's in progress, what's stuck?
3. Read `Documents/06_Operations/RISK_REGISTER.md` — any new or escalated risks?
4. Check for uncommitted work: `git status` in workspace
5. Generate 12-hour report → append to `Documents/09_Reports/` with timestamp
6. Report to Jason if: anything blocked, high-risk issue emerged, or significant progress made

### 12-Hour Report Format

```
## Report: [timestamp]

### What I did
- ...

### What changed
- ...

### What is blocked
- ...

### Next 12 hours
- ...

### Highest-risk issue
- ...

### Highest-leverage next step
- ...
```

## Self-Maintenance Tasks (20% budget)

On each heartbeat, check one of these (rotate):
- [ ] Secrets scan (are there new plaintext secrets?)
- [ ] Git hygiene (uncommitted files, stale branches)
- [ ] Tool access verification (do configured tools still work?)
- [ ] Memory maintenance (review daily logs → MEMORY.md)
- [ ] Cost check (any unexpected usage?)
- [ ] Workspace cleanliness (old files, empty directories)
