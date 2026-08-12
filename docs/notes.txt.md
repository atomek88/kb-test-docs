---
title: "Slug Round-Trip Guard"
status: current
last_reviewed: 2026-08-12
---

# Slug Round-Trip Guard

This is a **Markdown** file whose name ends in `.txt.md` (TDD §5.6).

`pathToSlug("docs/notes.txt.md")` must return `docs/notes.txt.md` — **not** `docs/notes.txt`,
which `slugToPath` would then resolve to a different (nonexistent) file. Its URL therefore
keeps the full `.txt.md`.

Do not edit: integration tests assert exact bytes.
