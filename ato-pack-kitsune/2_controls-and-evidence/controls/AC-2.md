# AC-2 — Account Management

## Summary
Kitsune manages user and privileged accounts through a documented lifecycle so that only authorized individuals have access, access matches job role/need-to-know, and access is removed promptly when no longer required.

---

## Implementation

### Allowed vs. prohibited account types
- **Allowed (by default):**
  - Individual user accounts (named users)
  - Privileged administrator accounts (separate from daily-use accounts)
  - Auditor / read-only review accounts (where required)
  - Service accounts (e.g., CI/build service), scoped and documented
- **Prohibited by default (requires explicit approval + conditions):**
  - Shared/group accounts
  - Anonymous/guest accounts
  - Temporary/emergency accounts (only if time-bound and formally approved)

### Account lifecycle workflow (request → approval → provisioning → review → removal)
1. **Request:** Access request submitted with justification (need-to-know), requested role(s), and system(s) in scope.
2. **Prerequisites:** Training/briefing requirements satisfied (as applicable) before provisioning.
3. **Approval:** System Owner approves account creation and any privileged role assignment.
4. **Provisioning:** Account Manager/Admin provisions the account in the fictional IdP/directory service and applies role/group membership.
5. **Modification:** Role changes follow the same approval path (especially for privileged roles).
6. **Disable/Remove:** Accounts are disabled/removed promptly upon termination/transfer, role change, policy violation, or when access is no longer required.

### Where account controls are enforced
- **Identity lifecycle:** Centralized in the fictional directory/IdP.
- **Authorization enforcement:** Services on the Kitsune LAN (e.g., source control, CI/build, artifact repository) enforce role/group membership and least privilege.
- **Privileged administration:** Performed from admin workstations using separate admin accounts.

### Who does what (roles)
- **System Owner:** Approves account creation and privileged access; owns risk decisions for exceptions.
- **Account Managers / LAN Admins:** Execute provisioning, modification, disabling, and removal actions.
- **ISSO:** Validates evidence exists and is complete; tracks noncompliance and POA&M items.
- **ISSM:** Provides final review / quality control for process adherence and inspection readiness.

---

## Reviews, monitoring, and auditability

### Account reviews (cadence)
- **All accounts:** reviewed at least **annually** (inventory + role validation).
- **Privileged/admin accounts:** recommended **quarterly** review (explicitly validate continued need).
- **Inactivity handling (example org-defined value):** disable accounts after **35 days** of inactivity *if documented in local policy/procedure*.

### Logging / auditing
- Account lifecycle events (create/modify/disable/remove), privilege changes, and authentication events are logged and forwarded to the central logging/SIEM capability.

---
## Evidence (public-safe examples)
- [Account provisioning workflow](../evidence/account-management-sample/account-provisioning-workflow.md)
- [Access review record](../evidence/account-management-sample/access-review_YYYY-MM-DD.md)
- (Optional) Ticket examples, account inventory export (fictional), privileged access list, and log review checklist.


## Evidence (public-safe examples)
- [Account provisioning workflow](../evidence/account-management-sample/account-provisioning-workflow.md)
- Access review record: `2_controls-and-evidence/evidence/account-management-sample/access-review_YYYY-MM-DD.md`
- (Optional) Ticket examples, account inventory export (fictional), privileged access list, and log review checklist.

---

## Exceptions (controlled)
Any exception (e.g., temporary account, emergency admin access, shared account for technical constraint) requires:
- documented justification,
- explicit approval,
- time-bound conditions, and
- evidence of closure/removal when no longer required.
