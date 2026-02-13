# SI-2 — Flaw Remediation (Patching)

## Summary
Kitsune remediates OS and software flaws on a defined cadence and tracks remediation status to maintain a secure baseline inside the isolated LAN.

---

## Implementation

### What
- Patches are applied for servers and workstations.
- Exceptions are documented (e.g., compatibility constraints) and tracked through POA&M.

### How
- Patches are staged through an **offline patch intake** process (fictional) appropriate for an air-gapped LAN.
- Patch status is validated via reports and/or scans.
- Critical vulnerabilities are prioritized and tracked to closure.

### Where
- Patch compliance summaries and scan summaries are stored as evidence artifacts.
- POA&M is used to track remediation actions, owners, and dates.

### Who
- LAN Admins apply patches and maintain patch staging.
- ISSO validates evidence and ensures findings are tracked; ISSM provides oversight.

### When / cadence (example)
- Monthly patch cycle (standard)
- Out-of-cycle patching for critical/high risk items as required

---

## Evidence (public-safe examples)
- Patch compliance summary: `2_controls-and-evidence/evidence/patch-compliance-sample/patch-compliance-summary.md`
- POA&M workflow: `3_poam/poam-workflow.md`
- Sample POA&M export: `3_poam/poam-sample.csv`
