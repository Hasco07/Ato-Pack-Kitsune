# System Description (Fictional)

**System name:** IS 2096 Kitsune (“Kitsune”)  
**System type:** Isolated Local Area Network (LAN) for software development / integration / test  
**Environment:** Air‑gapped / offline lab environment (fictional)  
**Primary security objective:** Prevent unauthorized disclosure or modification of sensitive program artifacts while enabling repeatable build/test workflows.

## Purpose
Kitsune is an isolated local area network (LAN) used to develop, integrate, and test software that supports classified jet programs. It provides a controlled environment where engineers can build and validate code without exposing sensitive data or connecting to external networks. The LAN is designed to mirror key aspects of the target aircraft/mission systems stack so teams can run builds, execute automated tests, and troubleshoot issues early.

## Users / Roles
- **Engineers / Developers:** Write code, run builds, execute tests, review results.
- **Build / Integration Engineers:** Maintain CI/build pipelines, artifact repositories, and test automation.
- **LAN Administrators:** Maintain servers, workstations, baseline configurations, backups, and account administration.
- **Security Roles (ISSO/ISSM equivalent):** Maintain SSP artifacts, validate evidence, manage POA&Ms, sustain inspection readiness.
- **Auditors / Assessors (fictional):** Review artifacts and evidence for authorization / compliance.

## Major components (high-level)
- **Developer workstations** (user and privileged admin accounts separated)
- **Source control server** (e.g., Git service – fictional)
- **Build/CI server** (build + test execution)
- **Artifact repository** (signed/hashed build outputs – fictional)
- **Test harness / simulator environment** (mirrors portions of mission stack – fictional)
- **Central logging / SIEM** (e.g., Splunk-like – fictional)
- **Vulnerability scanning host** (e.g., ACAS-like – fictional)
- **Directory services / IdP** (identity lifecycle + authentication – fictional)
- **Patch repository / staging** (offline patching workflow)

## System boundary
Included in the Kitsune boundary:
- The isolated Kitsune LAN (switching/routing within the lab)
- Workstations and servers used for development, build, test, logging, and scanning
- Administrative services required to operate the LAN (identity, patch staging, backups)

Explicitly excluded from the Kitsune boundary:
- Any production/operational aircraft or mission systems
- Enterprise networks and the public internet
- External cloud services (no direct connectivity)

## External connections
- **None by design (air-gapped).**
- Data transfer is only via **controlled, documented media transfer** processes (fictional) and is treated as a security-relevant event.

## Assumptions / constraints (for this public demo)
- All artifacts are **fictionalized** to demonstrate RMF structure and evidence traceability.
- No customer templates, real diagrams, hostnames, IPs, or screenshots are used.
