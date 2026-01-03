# Security Policy

This repository is part of a governance-first platform ecosystem.
Security issues include vulnerabilities that could impact:

- authentication / authorization
- permissions & role enforcement
- data access boundaries
- audit integrity
- governance enforcement (CODEOWNERS / workflows)
- supply chain safety (dependencies, CI workflows)
- secrets leakage (API keys, signing secrets, tokens)
- unsafe defaults that could enable bypass behavior

## Supported Versions

Security fixes are applied to the default branch (`main`) and active release branches (if any).
If this repo is archived or deprecated, it must be clearly marked in the README.

## Reporting a Vulnerability (Private)

Please do **not** open a public issue for security-sensitive reports.

Use one of the following private channels:
- GitHub **Security Advisories** (preferred): “Report a vulnerability” in this repo
- Direct message to the maintainer/owner listed in CODEOWNERS

When reporting, include:
- a clear description of the issue and impact
- steps to reproduce (PoC if safe)
- affected files/paths
- suggested fix (if known)

## Coordinated Disclosure

- We will acknowledge receipt as soon as we see it.
- We will triage severity (Critical/High/Medium/Low) and prioritize accordingly.
- We may request additional details to reproduce safely.
- Fixes will land behind PRs and required checks.
- Public disclosure happens **after** a fix is merged (or a mitigation is documented).

## Out of Scope

The following are generally out of scope unless they demonstrate real impact:
- best-practice suggestions without a concrete exploit path
- denial of service that requires unrealistic traffic/resources
- issues requiring privileged access that the platform does not grant
- purely theoretical cryptographic concerns without a practical vector

## Safe Harbor

Good-faith security research is welcome when it:
- avoids privacy violation and data exfiltration
- avoids service disruption
- avoids social engineering
- avoids accessing accounts or data you do not own
