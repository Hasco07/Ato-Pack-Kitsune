# MP-5 — Media Transport (Air-gapped Transfer)

## Summary
Because Kitsune is air-gapped, any import/export of data or updates is handled via controlled removable media procedures to prevent malware introduction, data spillage, and loss of accountability.

---

## Implementation

### What
- Only approved removable media is permitted for transfers into/out of the Kitsune LAN.
- Transfers are limited to mission/engineering need and follow documented approval + logging.

### How
- A controlled media transfer process is used (fictional):
  1) Request/approval (what, why, owner, destination/source, classification marking rules in the fictional context)
  2) Media preparation (labeling, inventory control; write protection where feasible)
  3) Malware scanning (before import; and before export if applicable)
  4) Transfer via controlled point only
  5) Logging and retention of transfer records
  6) Media sanitization/return to controlled storage (or destruction) per procedure

### Where
- All media movement is recorded in a media transfer log.
- Supporting artifacts (request/approval, scan record, manifest) are stored as evidence.

### Who
- **Requestor:** provides justification and intended content.
- **Approver (System Owner / delegate):** authorizes transfer.
- **Media Control Agent (fictional):** maintains inventory and executes procedure.
- **ISSO:** validates evidence and flags noncompliance; tracks issues in POA&M when needed.

### When / cadence
- Per transfer event (no “routine” transfer by default).
- Periodic review (e.g., monthly/quarterly) of media logs to validate process adherence.

---

## Evidence (public-safe examples)
- [Media transfer procedure](../evidence/media-transport-sample/media-transfer-procedure.md)
- [Media transfer log](../evidence/media-transport-sample/media-transfer-log_YYYY-MM-DD.md)
- [Malware scan record](../evidence/media-transport-sample/malware-scan-record_YYYY-MM-DD.md)
- [Approved media inventory](../evidence/media-transport-sample/approved-media-inventory.md)


---

## Notes (risk reduction)
- Keep transfers minimal and explicitly approved.
- Maintain chain-of-custody style accountability.
- Treat media as a primary threat vector for air-gapped environments.
