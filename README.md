# execblock

opinionated linter for config files. yaml, json, toml.

```
npm i -g execblock
```

check files:

```
execblock check config.yaml
```

rules:

- no tabs (use spaces)
- consistent quotes
- sorted keys (optional)
- trailing commas
- max line length 120

### auto-fix

```
execblock fix config.yaml
```

### ci integration

```yaml
# .github/workflows/lint.yml
- run: execblock check *.{yaml,json,toml}
```

### disable rules

```yaml
# .execblock.yaml
rules:
  sorted-keys: false
  max-line-length: 200
```

exit code 0 if pass, 1 if fail.
