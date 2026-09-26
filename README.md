# hwlog

Custom hardware log file type `.hwlog`.

**Repo:** https://github.com/fitzyracing1/hwlog  
**Pages:** https://fitzyracing1.github.io/hwlog/  
**AI discovery pack:** https://fitzyracing1.github.io/hwlog/ai-discovery/

Declared format. Not an OS MIME install.

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

## Pages

Site source is `docs/`. If the live URL 404s, enable Pages once:

GitHub repo → Settings → Pages → Source: GitHub Actions

## AI discovery pack

- `ai-discovery/pack.json`
- `ai-discovery/llms.txt`
- `ai-discovery/AGENTS.md`
- `ai-discovery/SKILL.md`

```bash
python3 scripts/validate-kind.py assets/hwlog.kind
```
