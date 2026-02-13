# AU-6 — Audit Review, Analysis, and Reporting

## Summary
Kitsune reviews and analyzes audit logs and security-relevant events to detect suspicious activity, validate control effectiveness, and support investigations and continuous monitoring.

---

## Implementation

### What
- Audit logs and alerts are reviewed for:
  - authentication anomalies (repeated failures, lockouts)
  - privilege/role changes
  - administrative actions on servers/workstations
  - logging failures or gaps (e.g., forwarding stopped)
  - vulnerability scan execution/results anomalies (unexpected spikes, missing coverage)
  - controlled media transfer events (if applicable)

### How
- Central logging/SIEM receives logs from in-boundary sources.
- Routine review is performed using a checklist to ensure consistency and traceability.
- Notable events are documented, triaged, and escalated as required.
- Confirmed issues become tracked actions (ticket/POA&M) until closed.

### Where
- Reviews are documented as evidence artifacts (weekly/monthly records).
- Leadership-facing summaries are captured in periodic briefs when appropriate.

### Who
- **ISSO:** performs routine review and alert triage; documents results.
- **ISSM:** oversight; ensures cadence is met and reporting is inspection-ready.
- **System Owner / Program Leadership (fictional):** receives risk summaries as needed.

### When / cadence (example)
- Daily/near-real-time: alert monitoring (if implemented)
- Weekly: log review sampling (auth/admin/high-risk events)
- Monthly: logging coverage validation and trend reporting

---

## Evidence (public-safe examples)
- [Log review checklist](../evidence/logging-config-sample/log-review-checklist.md)
- [Weekly log review record](../evidence/logging-config-sample/weekly-log-review_YYYY-MM-DD.md)
- [Alert triage playbook](../evidence/logging-config-sample/alert-triage-playbook.md)
- (Optional) [Monthly audit summary](../../5_briefs/executive-risk-brief.md)

---

## Reporting (what “good” looks like)
A good review record shows:
- date/time range reviewed,
- sources covered,
- anomalies observed (or “none observed”),
- actions taken / escalations,
- linkage to tickets/POA&M items when applicable.
