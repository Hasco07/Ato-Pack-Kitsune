# Continuous Monitoring Plan (Fictional)

## Purpose
Define how Kitsune sustains an authorization-ready posture over time by performing recurring monitoring activities, refreshing evidence, and tracking issues to closure.

> This is a **public-safe example** plan. Cadence values are fictional and can be adjusted.

---

## Monitoring activities (example cadence)

| Activity | Scope | Cadence | Owner | Evidence Location |
|---|---|---:|---|---|
| Alert monitoring / triage | SIEM alerts, critical events | Daily / near-real-time | SecOps / ISSO | `2_controls-and-evidence/evidence/logging-config-sample/` |
| Log review sampling | Auth + admin events | Weekly | ISSO | `2_controls-and-evidence/evidence/logging-config-sample/log-review-checklist.md` |
| POA&M triage | Open findings + overdue items | Weekly | ISSO / ISSM | `3_poam/` |
| Patch compliance review | In-boundary servers/workstations | Monthly | LAN Admins | `2_controls-and-evidence/evidence/patch-compliance-sample/` |
| Vulnerability scanning | Servers + workstations | Monthly (or quarterly for low-risk segments) | SecOps | `3_poam/` (findings tracked) |
| Privileged access review | Admin + service accounts | Quarterly (recommended) | System Owner + ISSO | `2_controls-and-evidence/evidence/account-management-sample/` |
| Full account inventory review | All accounts | Annually (minimum) | System Owner + ISSO | `2_controls-and-evidence/evidence/account-management-sample/` |
| Baseline/config review | Baselines + change history | Quarterly | LAN Admins + ISSO | `2_controls-and-evidence/evidence/change-control-sample/` |
| Self-inspection | Inspection readiness | Quarterly | ISSM | `4_self-inspections/` |

---

## Evidence refresh rules
- Evidence is stored under `2_controls-and-evidence/evidence/` with dated records where appropriate.
- Evidence is refreshed on the cadence above and whenever significant changes occur (boundary change, new server, major upgrade).
- All evidence should be easy to trace back to a control narrative.

---

## Reporting
- Weekly: POA&M triage notes + overdue/high-risk status
- Monthly: continuous monitoring status summary (top risks, trends, blockers)
- Quarterly: self-inspection summary + SSP delta review

See also: `4_self-inspections/inspection-readiness-runbook.md`
