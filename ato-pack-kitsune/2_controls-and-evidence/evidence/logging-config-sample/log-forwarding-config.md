# Log Forwarding Configuration (Fictional)

**Forwarding methods (examples):**
- Workstations/servers: agent or syslog forwarding (fictional)
- IdP/directory services: native audit log forwarding (fictional)
- CI/build tooling: pipeline audit logs forwarded (fictional)
- Scanner: scheduled scan summaries forwarded (fictional)

**Destination:**
- Central logging/SIEM: `KIT-LOG-01` (fictional)

**Retention (example):**
- Online searchable retention: 90 days (fictional)
- Archived retention: 1 year (fictional)

**Validation:**
- Daily heartbeat check to confirm sources are actively forwarding
- Alerts for missing log sources or sudden drop in event volume
