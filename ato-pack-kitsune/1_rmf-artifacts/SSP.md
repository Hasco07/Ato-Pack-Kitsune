# SSP (Public / Fictional)

> This is a **public-safe SSP-style** document. It demonstrates structure, clarity, and evidence traceability for an RMF/ATO package.
>
> **OPSEC / confidentiality:** No proprietary templates, customer identifiers, real diagrams, hostnames, IPs, or screenshots are included.

---

## 1. System Identification
- **System Name:** IS 2096 Kitsune
- **System Owner:** Hassan Biglari *(fictional for portfolio demonstration)*
- **Authorizing Official (fictional):** Government Authorizing Official (AO) (Fictional)
- **Assessor / Oversight (fictional):** DCSA (Assessment Support) (Fictional)
- **System Type:** Isolated Development & Integration LAN
- **System Categorization (fictional):** M-L-L (Fictional placeholder)

---

## 2. System Environment

### 2.1 System Purpose
Kitsune is an isolated local area network (LAN) used to develop, integrate, and test software that supports classified jet programs. It provides a controlled environment where engineers can build and validate code without exposing sensitive data or connecting to external networks. The LAN is designed to mirror key aspects of the target aircraft/mission systems stack so teams can run builds, execute automated tests, and troubleshoot issues early.

### 2.2 System Boundary

**Included components (in-boundary):**
- Kitsune LAN switching/routing within the lab
- Developer and administrator workstations
- Source control server, build/CI server, artifact repository
- Test harness / simulator environment
- Directory services / IdP
- Central logging/SIEM and vulnerability scanning host
- Offline patch staging and backup services (fictional)

**Excluded components (out-of-boundary):**
- Production/operational aircraft or mission systems
- Enterprise networks and the public internet
- External cloud services (no direct connectivity)

**External connections:**
- **None by design (air-gapped).**
- Any import/export uses a controlled media transfer process (fictional) and is logged/approved.

### 2.3 Data Types / Sensitivity (fictional)
- Software source code, build artifacts, and test outputs supporting a classified program
- Configuration baselines and change records
- Authentication/audit logs and security monitoring records

### 2.4 Users / Roles (fictional)
- Engineers / developers
- Build & integration engineers
- LAN administrators (separate privileged accounts)
- Security roles (ISSO/ISSM)
- Auditors / assessors (read-only review of evidence)

---

## 3. Control Baseline / Control Documentation Approach (public-safe)

### 3.1 Baseline (fictional)
- Controls are written to align conceptually with **NIST SP 800-53 Rev. 5** at a Moderate-like baseline (fictional).
- Additional classified-program expectations (e.g., JSIG-style constraints) are **referenced conceptually** without reproducing controlled overlays.

### 3.2 How controls are documented in this repo
Each control narrative aims to answer, in plain language:
- **What** is implemented (policy/requirement intent)
- **How** it is implemented (process + technical enforcement)
- **Who** performs the action (roles/responsibilities)
- **When** it happens (cadence + triggers)
- **What evidence** is produced (and where it lives in the repo)

Control narratives live here: `2_controls-and-evidence/controls/`  
Evidence examples live here: `2_controls-and-evidence/evidence/`

---

## 4. Continuous Monitoring Strategy (example)

- **Accounts (AC-2):** annual review minimum; privileged review recommended quarterly; disable promptly on separation/role change. *(Example org-defined value: disable after 35 days inactivity if documented.)*
- **Logging (AU family):** central log forwarding; routine review + alerting for security-relevant events.
- **Configuration management (CM-2):** baseline under version control; changes tracked and reviewed.
- **Patching (SI-2):** patch compliance tracked; exceptions documented; findings flow into POA&M.
- **Vulnerability scanning:** scheduled scanning of in-boundary components; findings triaged into POA&M.

See: `1_rmf-artifacts/continuous-monitoring-plan.md`

---

## 5. Supporting Plans (public-safe)
- Configuration Management Plan: `1_rmf-artifacts/configuration-management-plan.md`
- Incident Response Plan: `1_rmf-artifacts/incident-response-plan.md`
- Continuous Monitoring Plan: `1_rmf-artifacts/continuous-monitoring-plan.md`

---

## 6. POA&M (example)
- POA&M workflow: `3_poam/poam-workflow.md`
- Sample POA&M export: `3_poam/poam-sample.csv`

---

## 7. Diagrams / Inventory
- Boundary diagram: `0_system-overview/boundary-diagram.md`
- Data flow diagram: `0_system-overview/data-flow-diagram.md`
- Asset inventory: `0_system-overview/asset-inventory.md`
