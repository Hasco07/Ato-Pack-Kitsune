# Controlled Media Transfer Procedure (Fictional)

**System:** Kitsune LAN (Air-gapped)  
**Control:** MP-5  
**Goal:** Prevent malware introduction, data spillage, and loss of accountability.

## Roles
- **Requestor:** states what/why, provides content owner
- **Approver:** System Owner or delegate (fictional)
- **Media Control Agent:** issues media, maintains inventory/log
- **ISSO:** validates evidence completeness + reviews process adherence

## Procedure (import/export)
1) **Request**
   - Request includes: purpose, data description, source/destination, owner, required date
2) **Approval**
   - Approver authorizes transfer and conditions (time-bound as needed)
3) **Media preparation**
   - Use only approved media from inventory
   - Label media ID + record custody
4) **Malware scanning**
   - Scan media before import (and before export if applicable)
   - Record tool + signatures date + result
5) **Transfer**
   - Perform transfer only at the controlled transfer point (fictional)
6) **Logging**
   - Record: media ID, who, what, when, direction, approval reference
7) **Post-transfer handling**
   - Return media to controlled storage or sanitize per procedure

## Evidence produced
- Transfer log entry: `media-transfer-log_YYYY-MM-DD.md`
- Malware scan record: `malware-scan-record_YYYY-MM-DD.md`
- Inventory reference: `approved-media-inventory.md`
