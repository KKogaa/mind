---
title: Index
tags: [moc, index]
---

# Index

Top-level entry point. Browse by map of content (MOC):

| Map | Covers |
| --- | --- |
| [[azure]] | AZ-204, AI-900, AI-102 study notes |
| [[programming]] | Practice and building |
| [[goals]] | Roadmaps, todo lists, current commitments |
| [[finance]] | Cash flow and trading |
| [[health]] | Training, intake, body weight |
| [[lifestyle]] | Everything else |

## Folders

- `daily/` — daily notes
- `notes/` — atomic notes (flat)
- `maps/` — MOCs by topic
- `attachments/` — images and binary files

## Conventions

- **Frontmatter** — every note starts with `title`, `tags`, and `up` (the map it belongs to). Tags live in frontmatter, not as loose `#hashtag` lines in the body.
- **One H1** — the note title, matching the frontmatter `title`.
- **Atomic notes** — one topic per file in `notes/`, flat, no subfolders. Long notes get split and replaced by a hub note that links the pieces (see [[azure-ai-901]]).
- **Related section** — notes end with a `## Related` list linking sideways to sibling notes. Maps link down; notes link across.
- **Attachments** — all images live in `attachments/`, embedded with `![[filename.png]]`.
- **Todo lists** — kept separate by domain: [[things-todo]] (personal), [[work-things-todo]] (work), [[azure-study-todo]] (certification).
