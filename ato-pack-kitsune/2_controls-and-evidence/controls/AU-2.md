# AU-2 — Event Logging

## Summary
Kitsune defines and logs security-relevant events across the isolated LAN to support accountability, investigations, and continuous monitoring.

---

## Implementation

### What is logged (examples)
- Authentication events (success/failure), MFA events (if applicable)
- Account lifecycle events (create/modify/disable/remove) and privilege changes (AC-2/AC-6 support)
- Administrative actions on servers/workstations (e.g., configuration changes, service restarts)
- Source control actions (repo access, commits, branch changes) *(fictional)*
- Build/CI actions (build triggers, artifact publishing, test execution) *(fictional)*
- Vulnerability scan execution and summary results
- Patch installation events and patch compliance status
- Controlled media import/export events (if used)

### How logging is implemented
- OS and service logs are generated at the source (workstations/servers/services).
- Logs are forwarded to a central logging/SIEM capability for retention and review.
- Alerts are configured for high-risk events (e.g., repeated auth failures, privilege escalation, disabled logging).

### Where logs are stored
- Central logging/SIEM (fictional) is the authoritative repository for security event logs.

### Who reviews logs
- ISSO reviews alerts and performs routine log review sampling.
- Findings are documented and, when needed, tracked through POA&M.

### When / cadence (example)
- Daily/near-real-time: alert monitoring
- Weekly: sampling review of auth/admin events
- Monthly: review of logging coverage (sources onboarded, gaps, retention)

---

## Evidence (public-safe examples)
- Log source list: `2_controls-and-evidence/evidence/logging-config-sample/log-source-list.md`
- Log forwarding configuration summary: `2_controls-and-evidence/evidence/logging-config-sample/log-forwarding-config.md`
- Log review checklist: `2_controls-and-evidence/evidence/logging-config-sample/log-review-checklist.md`
