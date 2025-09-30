```md
### Title
<!-- Use Conventional Commits, e.g.: "feat: add Python test stage" -->

### Summary
<!-- 1–3 sentences: what changed and why. -->

### Linked Issue(s)
Closes #__

---

## Type
- [ ] fix
- [ ] feat
- [ ] docs
- [ ] chore
- [ ] refactor
- [ ] test
- [ ] ci

## Scope (check all that apply)
- [ ] Node (package.json)
- [ ] Python (requirements.txt / pyproject.toml)
- [ ] Go (go.mod)
- [ ] Rust (Cargo.toml)
- [ ] Java (Maven/Gradle)
- [ ] .NET (*.csproj)
- [ ] Docker (Dockerfile)
- [ ] Docs / Config

---

## Changes
<!-- Bullet list of key changes. Keep it crisp. -->
- …

### Screenshots / Logs (optional)
<!-- Paste relevant console output or images. -->
<details><summary>Show output</summary>

```

...

````
</details>

---

## Test Plan
- [ ] Unit tests added/updated (if applicable)
- [ ] Local run OK
- [ ] CI passes for all relevant jobs

<details><summary>How I tested locally</summary>

```bash
# clone & checkout
git clone https://github.com/xryv/anylang-repo-template
cd anylang-repo-template
git fetch --all
git checkout <this-branch>

# run tests (pick what applies)
npm test || true
python -m pytest -q || python -m unittest discover -v || true
go test ./... || true
cargo test || true
mvn -B test || ./gradlew test || true
dotnet test || true
````

</details>

---

## CI & Compatibility

* [ ] Node job green (if package.json present)
* [ ] Python job green (if requirements/pyproject present)
* [ ] Go job green (if go.mod present)
* [ ] Rust job green (if Cargo.toml present)
* [ ] Java job green (if Maven/Gradle present)
* [ ] .NET job green (if *.csproj present)
* [ ] Docker build OK (if Dockerfile present)

---

## Security / Permissions

* [ ] No new secrets
* [ ] GitHub Actions permissions are least‑privilege
* [ ] Dependencies reviewed (if added/updated)

---

## Documentation

* [ ] README updated
* [ ] CHANGELOG entry
* [ ] Comments/examples added where helpful

---

## Breaking Changes

* [ ] No
* [ ] Yes — migration notes below

**Migration notes (if any):**

```
...
```

---

## Checklist (final)

* [ ] Title follows Conventional Commits
* [ ] Linked issue referenced
* [ ] Clear, reproducible steps provided
* [ ] All relevant CI checks are green

```
::contentReference[oaicite:0]{index=0}
```
