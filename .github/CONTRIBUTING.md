# Contributing

This repository is governed software.
Contributions must preserve:

- platform governance hierarchy
- permission boundaries
- audit integrity
- non-bypassable enforcement at the correct layer (DB/infra before UI)
- deterministic, reviewable change history

If you are not aligned with governance-first development, do not contribute.

---

## 1) Non-Negotiable Rules

### Governance & Authority
- Governance documents are binding within this repo’s scope.
- If a rule is not committed to Git, it has no enforceable standing here.
- Implementation must never contradict the repo’s governance router/index (if present).

### No Silent Power
- No bypass flags, backdoors, hidden admin surfaces, or “temporary overrides”.
- No undocumented privileged paths.
- No shadow “service role” assumptions.

### Auditability
- Changes that affect permissions, data access, or governance must be:
  - explicitly documented in the PR description
  - testable (or at minimum, verifiable via checks)
  - reviewable by CODEOWNERS (when configured)

---

## 2) How to Contribute (Required Process)

### Branching
- Create a feature branch from `main`.
- Do not push directly to `main` (unless you are the sole maintainer and intentionally allow it).

### Pull Requests
All changes must go through a PR unless the repo explicitly documents an exception.

PRs must include:
- **What changed**
- **Why it changed**
- **Risk assessment**
- **Rollback plan** (even if “revert PR”)

If the change touches governance, permissions, workflows, or security boundaries:
- include the governance checklist in the PR template
- reference the governing file(s) that authorize the change

### Reviews
- If CODEOWNERS exists, required owners must approve.
- Do not self-merge changes that alter governance enforcement unless you are the designated owner.

---

## 3) What Requires Extra Scrutiny

These changes are considered high-impact and must be treated as such:
- permissions / role mapping changes
- auth/session changes
- data access boundary changes
- audit log changes
- workflow or CI changes that affect enforcement
- dependency upgrades that introduce new privilege or network behavior
- new telemetry, analytics, or observability hooks
- any “engine registry”, “vertical registry”, or cross-module routing logic

---

## 4) Code Quality Standards

- Prefer explicitness over cleverness.
- Avoid magic behavior and hidden defaults.
- Do not introduce breaking changes without documenting migration/compatibility behavior.
- Keep changes minimal and review-friendly.

---

## 5) Secrets & Credentials

- Never commit secrets.
- Never paste tokens/keys into issues/PRs.
- Use GitHub Secrets for CI.
- If you suspect a secret leak, rotate it immediately and follow `SECURITY.md`.

---

## 6) Final Statement

By contributing, you affirm:
- you will not bypass governance enforcement
- you will not introduce silent privilege or hidden access paths
- you accept that review and auditability override speed or convenience
