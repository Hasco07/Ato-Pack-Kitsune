# Vulnerability Scan Summary (Fictional) — YYYY-MM-DD

**System:** Kitsune LAN  
**Control:** RA-5  
**Scan type:** Credentialed (preferred)  
**Scanner:** KIT-SCAN-01 (Fictional)  
**Reviewer:** ISSO / SecOps (Fictional)

## Targets scanned
- Server Zone: KIT-IDP-01, KIT-GIT-01, KIT-CI-01, KIT-ART-01, KIT-TEST-01
- Workstations: KIT-WS-DEV-* (sample), KIT-WS-ADM-* (sample)

## Coverage validation
- Authenticated scanning: ✅ Yes (servers) / ⚠️ Partial (workstations sampled)
- Exceptions (if any): (none) / (list and justify)

## Results (summary)
| Severity | Count | Notes |
|---|---:|---|
| Critical | 0 |  |
| High | 2 | Example: missing patch / insecure config |
| Medium | 5 | Example: hardening deltas |
| Low | 9 | Example: informational |

## Top findings (examples)
1) **High:** Missing security update on KIT-CI-01  
   - Owner: Engineering Tools  
   - Target date: YYYY-MM-DD  
   - Tracking: POAM-001 (fictional)

2) **High:** Misconfiguration on KIT-GIT-01 (audit policy drift)  
   - Owner: Engineering Tools  
   - Target date: YYYY-MM-DD  
   - Tracking: POAM-00X (fictional)

## Actions taken
- Findings triaged and assigned owners
- POA&M updated with due dates and mitigation notes
- Next scan scheduled per cadence
