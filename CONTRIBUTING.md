# Contributing to `anylang-repo-template` 🚀

Welcome! Whether you're fixing a typo, adding support for a language, or improving CI workflows — your contribution matters.  
This guide explains how to propose changes and what we expect from contributors.

---

## 🔧 Project Philosophy

This repository is:

- Language‑agnostic → supports any language, only runs what matters.
- Zero‑bloat → no lock-in, no dependencies unless needed.
- Instantly useful → clone & launch in < 60 seconds.
- Readable → CI and config should be easy to audit.

Contributions should follow the same spirit.

---

## 🧭 Getting Started

1. **Fork** the repo → https://github.com/xryv/anylang-repo-template/fork
2. **Clone** your fork:
   ```bash
   git clone https://github.com/<you>/anylang-repo-template
   ```

3. **Create a branch**:

   ```bash
   git checkout -b feat/add-ruby-support
   ```

---

## 🧪 Running Tests

Only run the tests relevant to the files you’ve touched:

| Language | Command                        |
| -------- | ------------------------------ |
| Node     | `npm test` or `node index.js`  |
| Python   | `pytest` or `unittest`         |
| Go       | `go test ./...`                |
| Rust     | `cargo test`                   |
| Java     | `mvn test` or `./gradlew test` |
| .NET     | `dotnet test`                  |
| Docker   | `docker build .`               |

---

## 📦 Commit Conventions

Use [Conventional Commits](https://www.conventionalcommits.org):

```
<type>(optional scope): <description>
```

Examples:

* `feat(ci): add Rust job`
* `fix: correct Java test fallback logic`
* `docs: improve README badges`

Common types:

* `feat` – new feature
* `fix` – bug fix
* `docs` – docs only
* `chore` – tooling/config
* `refactor` – code change w/o behavior change
* `ci` – workflow/config updates
* `test` – add or update tests

---

## 📂 Directory Structure

| Path                      | Purpose                           |
| ------------------------- | --------------------------------- |
| `.github/workflows/`      | CI logic per language             |
| `.github/ISSUE_TEMPLATE/` | Bug + feature templates           |
| `.editorconfig`           | Universal formatting rules        |
| `.gitattributes`          | Git-level encoding & EOL handling |
| `.gitignore`              | Build & IDE junk filters          |
| `CHANGELOG.md`            | History of changes                |
| `README.md`               | Overview and usage guide          |

---

## ✅ Pull Request Checklist

* [ ] Clear title using Conventional Commit
* [ ] Description explains **why** the change exists
* [ ] Linked to an issue (`Closes #123`)
* [ ] Only modifies relevant workflows / configs
* [ ] All CI jobs pass
* [ ] Docs updated if needed (`README.md`, `CHANGELOG.md`)

---

## 🛡 Code of Conduct

All contributors must abide by our [Code of Conduct](./CODE_OF_CONDUCT.md).

---

## 💬 Need help?

Start a Discussion or open an Issue:

* [https://github.com/xryv/anylang-repo-template/discussions](https://github.com/xryv/anylang-repo-template/discussions)
* [https://github.com/xryv/anylang-repo-template/issues/new/choose](https://github.com/xryv/anylang-repo-template/issues/new/choose)

---

Thanks for making this template better! 🌍

```
```
