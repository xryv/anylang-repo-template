# Changelog
All notable changes to **xryv/anylang-repo-template** will be documented here.  
Format follows **Keep a Changelog** and **Semantic Versioning**. Dates use **DD/MM/YYYY**.

---

## [Unreleased]
### Added
- (placeholder) …

### Changed
- (placeholder) …

### Fixed
- (placeholder) …

### CI
- (placeholder) …

### Security
- (placeholder) …

---

## [0.1.0] — 30/09/2025
### Added
- Multi‑language CI that auto‑detects stacks and runs only what’s relevant:
  - Node (npm), Python (pip/pytest/unittest), Go, Rust, Java (Maven/Gradle), .NET, Docker build
  - Docs job to ensure `README.md` exists
- Code scanning via **CodeQL** (JS/TS, Python, Go)
- Automated **releases** on `v*` tags with optional artifact bundling
- **Dependabot** for npm, pip, gomod, cargo, maven, gradle, nuget, docker, actions
- Project governance & docs: `CODEOWNERS`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, `CHANGELOG.md`, `CITATION.cff`, `LICENSE`, `FUNDING.yml`
- Issue & PR hygiene: `.github/ISSUE_TEMPLATE/{bug,feature}.md`, `config.yml`, `PULL_REQUEST_TEMPLATE.md`
- Editor & repo hygiene: `.editorconfig`, `.gitattributes`, `.gitignore`, `.prettierrc`, `.nvmrc`

### CI
- Node uses cached installs and respects `package-lock.json`
- Python job gracefully falls back to `unittest` if `pytest` is absent
- Rust job retries without `--locked` if needed
- Java supports both Maven and Gradle; Java 21 via Temurin
- Release job zips common artifact directories when present

### Security
- Least‑privilege workflow permissions
- Private security advisories link in Issue config

---

## Legend
- **Added** — new capabilities
- **Changed** — updates to existing behavior
- **Fixed** — bug fixes
- **CI** — build/test/release pipeline updates
- **Security** — security‑relevant changes

---

[Unreleased]: https://github.com/xryv/anylang-repo-template/compare/v0.1.0...HEAD
[0.1.0]: https://github.com/xryv/anylang-repo-template/releases/tag/v0.1.0
