# hwlog

Custom hardware log file type `.hwlog`.

**Repo:** https://github.com/fitzyracing1/hwlog

Append-only prototype log. One ENTRY block per update. Phone dictation maps onto STATUS, PROGRESS, PART, BOM, BLOCKER, NEXT.

This is a declared format, not an OS MIME install.

Sibling type: [keepn](https://github.com/fitzyracing1/keepn)

## Banner

```
# hwlog v1
```

## Example

```
# hwlog v1
---
PROJECT: Tesla Bot Cruiser
RIG: garage bay
---
ENTRY: 1
STATUS: Prototyping
PROGRESS: 12
PART: modular hull panel A
BOM: interlocking edge clips x8
NEXT: dry-fit panel A to rail
```

## Rules

- Line 1 must be `# hwlog v1`
- Frontmatter must include PROJECT
- Entries are numbered; append only; never rewrite a prior ENTRY
- STATUS is one of Concept, Design, Prototyping, Testing, Production Ready, Complete, On Hold
- PROGRESS is 0-100
- Allowed keys: STATUS, PROGRESS, PART, BOM, SOURCE, BLOCKER, NEXT, NOTE, RIG, SEQ

## Validate the declaration

```bash
python3 scripts/validate-kind.py assets/hwlog.kind
```

## Layout

- `assets/hwlog.kind` — type declaration
- `examples/sample.hwlog` — valid sample
- `scripts/validate-kind.py` — declaration validator
