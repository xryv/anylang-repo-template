---
name: "Bug report 🐛 (HERMETIC)"
about: "Zero‑ambiguity bug template. Fill every field. Do not delete sections."
title: "[BUG] <one‑line summary>"
labels: ["bug"]
assignees: []
---

<!--
READ FIRST 
1) Fill EVERY section below. If something doesn't apply, write "N/A".
2) Paste RAW logs/outputs (trim secrets). No screenshots for logs.
3) Keep commands copy‑pastable. Repro must work on a clean machine/CI.
-->

## TL;DR (one line)
<!-- e.g., "Python tests fail on Ubuntu in CI: ImportError for package X" -->
...

---

## Impact & Scope
- Severity:
  - [ ] 🔴 Critical — CI red or data loss
  - [ ] 🟠 Major — feature unusable for most users
  - [ ] 🟡 Moderate — degraded experience
  - [ ] 🟢 Minor — cosmetic/docs
- Affected domains (check all that apply):
  - [ ] Node (package.json)
  - [ ] Python (pyproject/requirements)
  - [ ] Go (go.mod)
  - [ ] Rust (Cargo.toml)
  - [ ] Java (Maven/Gradle)
  - [ ] .NET (*.csproj)
  - [ ] Docker (Dockerfile)
  - [ ] CI/Workflows
  - [ ] Docs / Config

---

## Commit & CI Links
- First bad commit SHA: `...`
- Branch: `...`
- Failing CI run URL: `https://github.com/xryv/anylang-repo-template/actions/runs/...`
- Failing job name (from CI): `...`

---

## Reproduction Protocol (copy‑paste exact steps)
> Repro MUST pass on a **fresh clone** and a **vanilla runner**.

```bash
# 1) Clean clone
git clone https://github.com/xryv/anylang-repo-template
cd anylang-repo-template
git fetch --all --tags
git checkout <SHA-or-branch>

# 2) Prepare toolchain ONLY if relevant (pick your stack)
# Node
if [ -f package.json ]; then npm ci || npm install; fi
# Python
if [ -f requirements.txt ]; then python -m pip install -r requirements.txt; fi
# Go
if [ -f go.mod ]; then go mod download; fi
# Rust
if [ -f Cargo.toml ]; then cargo fetch; fi
# Java
if ls | grep -Eq 'pom\.xml|build\.gradle'; then echo "JDK 21 required"; fi
# .NET
if ls *.csproj 1>/dev/null 2>&1; then dotnet restore; fi
# Docker
if [ -f Dockerfile ]; then docker build -t repro . || true; fi

# 3) Reproduce the failure (exact commands you ran)
# Replace the following with the real sequence:
npm test || true
# or: python -m pytest -q || true
# or: go test ./... || true
# or: cargo test || true
# or: mvn -B test || ./gradlew test || true
# or: dotnet test || true
