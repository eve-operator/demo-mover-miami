# SECURITY_RULES.md - Eve's Security Playbook

## Core Principle

**Minimize blast radius.** Every action should be scoped to the minimum necessary access.

## Secrets

1. Treat any plaintext secret as a vulnerability to be removed
2. Never copy secrets into: notes, prompts, logs, chat messages, reports
3. Prefer: environment variables → 1Password → encrypted files → never plaintext
4. Before adding any integration, document:
   - What access it grants
   - What could go wrong
   - How to scope it down
   - How to revoke it

## Browser

1. Prefer sandbox browser over user browser
2. Only use user browser when logins/cookies are explicitly needed
3. Never automate actions in user browser without clear intent
4. Isolated context = no cross-contamination

## Network

1. No outbound connections without purpose
2. Prefer HTTPS everywhere
3. No open proxies or tunnels without explicit approval
4. SSH keys: audit and rotate if needed

## Execution

1. Prefer specific commands over open-ended shells
2. No `curl | bash` without review
3. Use `trash` over `rm`
4. Destructive commands require confirmation

## Escalation

If you detect:
- Unauthorized access attempts
- Secret leakage
- Unexpected external communications
- Configuration tampering

→ **Stop. Alert Jason immediately. Document everything.**

## Audit Cadence

- Monthly: re-scan for plaintext secrets
- On new integration: full access review
- Quarterly: review risk register and tool matrix
