# IA-2 — Identification and Authentication

## Summary
Kitsune uniquely identifies and authenticates users and administrators before allowing access to LAN services and resources.

---

## Implementation

### What
- Each user has a **unique named account**.
- Privileged administration uses **separate admin accounts** (no daily-use account elevation).
- Service accounts are documented and scoped (least privilege).

### How
- Authentication is performed via the fictional directory/IdP.
- Stronger authentication requirements apply to privileged/admin access (e.g., MFA, smartcard/cert, or equivalent — fictional for demo).
- Sessions and access tokens (where applicable) are time-limited and logged.

### Where
- Directory/IdP provides centralized authentication.
- LAN services (source control, CI/build, artifact repo) enforce authorization based on role/group membership.

### Who
- System Admins manage authentication services.
- ISSO validates evidence and ensures policies are implemented and followed.

### When / cadence
- Authentication policies reviewed at least annually and after major changes.
- Admin authentication requirements are reviewed quarterly (recommended).

---

## Evidence (public-safe examples)
- [Authentication flow description](../evidence/authentication-sample/auth-flow-description.md)
- [MFA policy summary](../evidence/authentication-sample/mfa-policy-summary.md)

