# Security Policy

We take security seriously. If you discover a vulnerability, please follow the process below so we can fix it quickly and responsibly.

---

## Supported Versions

This template is a rolling project; security fixes target the default branch (`main`).  
If you’ve forked it for a specific project, apply upstream patches to your fork.

| Version | Supported |
|--------:|:---------:|
| `main`  | ✅        |
| tags `v*` | ✅ (best‑effort backport if practical) |

---

## How to Report a Vulnerability

**Please do not open a public issue for security reports.**

- **Private advisory (preferred):**  
  https://github.com/xryv/anylang-repo-template/security/advisories/new
- **Email (fallback):**  
  security@nowhere.invalid

When reporting, include:

- A clear description of the issue and **impact**
- **Reproduction steps** (copy‑pastable commands, minimal PoC)
- **Affected files/workflows** (paths and versions/commits)
- Any relevant logs, stack traces, or screenshots (sanitize secrets)
- Suggested fix or mitigation (optional but appreciated)

---

## What to Expect (Response & Timeline)

We aim to acknowledge reports within **48 hours** and keep you updated as we investigate.

Typical flow:

1. **Triage** – Validate, classify severity, confirm scope.  
2. **Mitigation** – Prepare fix, tests, and docs; evaluate backports.  
3. **Coordinated disclosure** – We’ll agree on a timeline (commonly 7–21 days) before public release, depending on severity and ecosystem impact.  
4. **Release** – Patch is merged to `main`, advisory published, a new tag is cut if warranted.  
5. **Credit** – With your consent, we can acknowledge your contribution in release notes/advisory.

---

## Scope & Threat Model

This repository contains **template code and GitHub workflows**. Security reports may relate to:

- CI workflows permissions (least‑privilege, token scopes)
- Supply‑chain hygiene (action pinning, provenance)
- Insecure defaults in example configs
- Scripts or docs that could lead users to unsafe practices

Reports **out of scope** typically include:

- Social engineering, spam, or non‑actionable “best practice” lists
- Issues requiring administrative access to your forked repo
- Vulnerabilities in third‑party actions or tools (report upstream)

---

## Hardening Guidelines (for users of this template)

- **Pin actions** to major versions (already done here; pin to SHAs for high assurance).  
- Use **environment‑scoped** or **OIDC‑federated** secrets where possible.  
- Keep `GITHUB_TOKEN` permissions minimal in workflows (`permissions:` blocks).  
- Review Dependabot PRs and CodeQL alerts promptly.  
- Rotate secrets and audit repository access regularly.

---

## Disclosure Policy

We follow **coordinated disclosure**. Please refrain from sharing details publicly until a fix is available. If an issue is already public, contact us anyway so we can prioritize remediation.

---

## Hall of Thanks

We’re grateful to researchers and contributors who help keep this project safe. If you’d like recognition, let us know in your report.

---
