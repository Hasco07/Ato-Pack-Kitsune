# Vulnerability Scan Schedule (Fictional)

**System:** Kitsune LAN (Air-gapped / Offline)  
**Control:** RA-5  
**Owner:** SecOps / Scanner Operator (Fictional)  
**Scanner Host:** KIT-SCAN-01 (Fictional)

## Scope (in-boundary targets)
- Developer workstations (sampled where appropriate)
- Admin workstations
- Servers: IdP, Git, CI, Artifact Repo, Test Harness
- Security tooling: logging/SIEM host, scanner host (self-scan as permitted)
- Offline patch staging host (if in boundary)

## Cadence (example)
- **Weekly (credentialed):** Server Zone targets (IdP/Git/CI/Art/Test)
- **Monthly (full):** All in-boundary targets + authenticated coverage validation
- **After major change:** Out-of-cycle scan following baseline or architecture change
- **After offline signature update:** Verify new checks are applied

## Scanner updates (air-gapped handling)
- Signature/content updates imported via controlled media transfer (see MP-5 process)
- Update event is logged and retained as part of scan evidence

## Evidence produced each cycle
- Scan results summary: `scan-summary_YYYY-MM-DD.md`
- Remediation status snapshot: `remediation-status_YYYY-MM-DD.md`
- POA&M updated for any new or overdue High/Critical findings
