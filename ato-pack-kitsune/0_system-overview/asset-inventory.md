# Asset Inventory (Fictional)

> Keep this lightweight. Reviewers care that you track **components, owners, and purpose**.

| Asset ID | Type | OS/Platform | Purpose | Owner | Notes |
|---|---|---|---|---|---|
| KIT-WS-DEV-* | Workstations | Windows / Linux (fictional) | Developer workstations (user accounts) | Engineering | Separate admin accounts used when required |
| KIT-WS-ADM-* | Workstations | Windows / Linux (fictional) | Admin workstations (privileged administration) | IT / LAN Admins | Used for IdP/server administration |
| KIT-IDP-01 | Server | Windows Server / Linux (fictional) | Directory services / IdP | IT / LAN Admins | Central authentication + account lifecycle |
| KIT-GIT-01 | Server | Linux (fictional) | Source control server | Engineering Tools | Logs forwarded to SIEM |
| KIT-CI-01 | Server | Linux (fictional) | Build/CI server | Engineering Tools | Executes builds + automated tests |
| KIT-ART-01 | Server | Linux (fictional) | Artifact repository | Engineering Tools | Stores build outputs |
| KIT-TEST-01 | Server/Appliance | Linux / Appliance (fictional) | Test harness / simulator | Integration Team | Mirrors aspects of mission stack |
| KIT-LOG-01 | Service | Splunk-like (fictional) | Central logging / SIEM | SecOps | Receives auth, admin, build/test, and scan logs |
| KIT-SCAN-01 | Server | Scanner appliance (fictional) | Vulnerability scanning | SecOps | Scheduled scans; results reviewed on cadence |
| KIT-PATCH-01 | Server | Repo service (fictional) | Offline patch staging | IT / LAN Admins | Controlled patch ingestion |
| KIT-BACKUP-01 | Service | Backup tool (fictional) | Backups / restores | IT / LAN Admins | Protects critical servers and configs |
