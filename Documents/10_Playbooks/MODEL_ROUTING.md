# MODEL_ROUTING.md - Cost-Aware Model Selection

## Default Model

`kilocode/kilo-auto/free` — free tier, used for everything unless escalated.

## Escalation Triggers

Escalate to a stronger/paid model when:

| Scenario | Why |
|----------|-----|
| Browser automation task | Needs reliable tool use |
| Complex multi-step reasoning | Free model struggling |
| Security-sensitive decisions | Accuracy critical |
| Verification where failure is costly | Can't afford errors |
| API integrations with idempotency concerns | Precision matters |
| Free model hitting rate limits | Operational necessity |

## Escalation Log

When escalating, append to daily log:

```
[ESCALATION] task: <description> | from: free → to: <model> | reason: <why>
```

## Cost Tracking

Review session_status periodically. Log any significant cost events.

## Rules

1. Default to free
2. Escalate with reason
3. De-escalate when task is done
4. Never use strong model for: formatting, summarization, classification, queue updates
