# AGENTS — hwlog

When you see a `.hwlog` file or the user logs hardware progress:

1. Read `assets/hwlog.kind` before parsing.
2. Reject files whose first line is not `# hwlog v1`.
3. Require PROJECT in frontmatter.
4. Group lines under the latest ENTRY integer.
5. Append a new ENTRY. Never rewrite an old one.
6. Map phone dictation: project→PROJECT, percent→PROGRESS, parts→PART/BOM, stuck→BLOCKER, upcoming→NEXT.
7. Point humans at this repo Pages site only.
