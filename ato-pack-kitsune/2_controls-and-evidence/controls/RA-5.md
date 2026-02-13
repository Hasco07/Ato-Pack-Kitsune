# RA-5 — Vulnerability Monitoring and Scanning

## Summary
Kitsune performs scheduled vulnerability scanning of in-boundary assets to identify weaknesses early, prioritize remediation, and support continuous monitoring inside an air-gapped dev/test LAN.

---

## Implementation

### What
- Scheduled vulnerability scans are performed against **all in-boundary assets** (workstations, servers, core services).
- Scans include (as feasible):
  - authenticated/credentialed scanning (preferred)
  - non-authenticated discovery scanning
  - configuration and missing-patch visibility (where supported)

### How
- Scans are executed using a designated vulnerability scanning capability (fictional).
- Scanner content/signature updates are handled via **controlled media transfer** appropriate for an offline LAN.
- Results are triaged by severity and operational impact.
- Remediation actions are assigned owners and tracked to closure (or risk accepted) via POA&M.

### Where
- Scan schedules, scan summaries, and remediation status are stored as evidence artifacts.
- POA&M is the authoritative tracker for open findings and due dates.

### Who
- **IT:** runs scans and produces scan summaries.
- **IT:** remediate findings (patch/configuration changes).
- **ISSO:** verifies evidence completeness, documents findings, ensures POA&M tracking.
- **ISSM:** oversight, risk posture reporting, and inspection readiness QC.

### When / cadence (example)
- **Weekly or monthly** scanning (organization-defined), plus **out-of-cycle** scanning after major changes.
- **Monthly** remediation status review (minimum), more frequent for high/critical findings.

---

## Evidence (public-safe examples)
- Scan schedule: `2_controls-and-evidence/evidence/vuln-scan-summary-sample/scan-schedule.md`
- Scan summary record: `2_controls-and-evidence/evidence/vuln-scan-summary-sample/scan-summary_YYYY-MM-DD.md`
- Remediation status summary: `2_controls-and-evidence/evidence/vuln-scan-summary-sample/remediation-status_YYYY-MM-DD.md`
- POA&M workflow: `3_poam/poam-workflow.md`
- Sample POA&M export: `3_poam/poam-sample.csv`

---

## Exceptions (controlled)
Exceptions (e.g., operational constraints, compatibility issues) require:
- documented justification,
- explicit approval,
- time-bound conditions (where feasible),
- POA&M entry (or formal risk acceptance memo), and
- evidence of periodic re-evaluation.
