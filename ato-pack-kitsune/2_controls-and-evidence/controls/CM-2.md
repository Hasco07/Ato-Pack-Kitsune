# CM-2 — Baseline Configuration

## Summary
Kitsune maintains documented baselines for in-boundary components (workstations, servers, and core services) to reduce configuration drift and enable repeatable compliance.

---

## Implementation

### What is baselined (examples)
- Workstation baseline (user vs admin workstation configuration)
- Server baseline (IdP, source control, CI/build, artifact repository, logging)
- Core security configurations (logging enabled, audit policies, account policies)
- Approved software list / installed packages (fictional summary)

### How baselines are controlled
- Baseline documentation is version-controlled.
- Changes follow the configuration management process and are reviewed/approved prior to implementation.
- Standardized naming and version history make it easy to demonstrate “what changed and why.”

### Where baselines live
- Baseline descriptions and change history live in this repo as public-safe summaries.

### Who approves changes
- CCB's approve operational changes.
- ISSO/ISSM validates documentation quality and evidence completeness prior to assessment.

### When / cadence
- Baselines reviewed at least annually and when significant changes occur.
- Emergency changes are documented and retrospectively reviewed.

---

## Evidence (public-safe examples)
- [Change ticket example](../evidence/change-control-sample/change-ticket-example.md)
- [Baseline version history](../evidence/change-control-sample/baseline_version_history.md)
- [Configuration Management Plan](../../1_rmf-artifacts/configuration-management-plan.md)

