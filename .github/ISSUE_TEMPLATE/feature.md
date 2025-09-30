---
name: "Feature request 🚀"
about: "Propose a capability with zero ambiguity. Fill every section. No deletions."
title: "[FEAT] <concise capability name>"
labels: ["enhancement"]
assignees: []
---

<!--
READ FIRST
1) Fill EVERY section. If N/A, write "N/A".
2) Be specific: measurable outcomes, concrete interfaces, copy‑pastable examples.
3) Treat this like an engineering spec. Clarity now saves weeks later.
-->

## TL;DR (one sentence)
<!-- e.g., "Add optional Python test stage that runs only when requirements.txt or pyproject.toml is present." -->
...

---

## Problem statement (why)
- Current behavior / gap:
- Who is affected:
- Business/technical impact:
- Evidence (issues, discussions, user quotes, CI logs):

---

## Goals (what this delivers)
- [ ] Goal 1 (measurable)
- [ ] Goal 2 (measurable)

### Non‑Goals (explicitly out of scope)
- Not doing:
- Also not doing:

---

## User stories
- As a <role>, I want <capability>, so that <value>.
- As a <role>, I need <signal/feedback>, so that <decision>.

---

## Proposed solution (overview)
Describe the approach in 3–7 sentences. Include constraints, invariants, and how it plays with existing workflows.

---

## Interface & schema (copy‑paste ready)
> Update or add only the sections that apply.

### 1) CI workflow changes (`.github/workflows/ci.yml`)
```yaml
# Example fragment (edit with your proposal)
jobs:
  python:
    if: ${{ hashFiles('**/pyproject.toml') != '' || hashFiles('**/requirements.txt') != '' }}
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with: { python-version: '3.12', cache: 'pip' }
      - run: python -m pip install --upgrade pip
      - run: |
          if [ -f requirements.txt ]; then pip install -r requirements.txt; fi
      - run: |
          if command -v pytest >/dev/null 2>&1; then pytest -q; else python -m unittest discover -v; fi
