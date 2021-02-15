---
id: git-hooks
title: git hooks
---

You can use HTMLHint as a git hook via the [pre-commit](https://github.com/pre-commit/pre-commit) framework.

Example for a basic `.pre-commit-config.yaml`:

```yaml
- repo: https://github.com/htmlhint/HTMLHint
  rev: # ref you want to point at, e.g. v0.14.2
  hooks:
    - id: htmlhint
```

Note that you can pass all arguments available for the [cli](../usage/cli#options) via the `args` option:

```yaml
- repo: https://github.com/htmlhint/HTMLHint
  rev: # ref you want to point at, e.g. v0.14.2
  hooks:
    - id: htmlhint
      args: ['--rules tag-pair,id-class-value=underline']
```
