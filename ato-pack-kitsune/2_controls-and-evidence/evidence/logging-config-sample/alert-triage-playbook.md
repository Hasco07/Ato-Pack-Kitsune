# Alert Triage Playbook (Fictional)

**System:** Kitsune LAN  
**Applies to:** AU-6 (review/analysis/reporting), IR support (conceptual)

## Triage priorities (example)
- **P1 (Immediate):** suspected credential compromise, privilege escalation, malware indicators, logging disabled
- **P2 (Same day):** repeated auth failures, new admin accounts, unexpected config changes
- **P3 (Routine):** policy drift, low-confidence detections, informational alerts

## Steps (fast + repeatable)
1) **Validate alert**
   - Confirm it’s not a test/noise
   - Identify impacted asset(s), user(s), and time range

2) **Scope**
   - Pivot on user, host, and timeframe
   - Check adjacent logs (IdP + admin + service logs)

3) **Contain (if applicable)**
   - Disable/lock account (AC-2/IA-2)
   - Isolate host (fictional LAN action)
   - Preserve evidence (export relevant log slices)

4) **Document**
   - Create ticket with: summary, timeline, affected scope, initial assessment
   - Link to control(s) impacted and evidence paths

5) **Escalate**
   - Notify System Owner/ISSM for P1/P2
   - Open POA&M item if control gap is identified

## Evidence to capture
- Alert screenshot/export (sanitized)
- Query used + results
- Actions taken and timestamps
- Ticket reference and closure notes
