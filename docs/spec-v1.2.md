---
title: "Versioned Filename URL Guard"
status: current
last_reviewed: 2026-08-12
---

# Versioned Filename URL Guard

A normal Markdown doc whose filename contains a dot-number (`v1.2`). This is the
**regression guard on existing URLs** (TDD §5.6).

A naive "does this path have an extension?" check reads the trailing `.2` as an extension
and stops stripping `.md`, silently moving this doc from `/docs/docs/spec-v1.2` to
`/docs/docs/spec-v1.2.md` and breaking every existing link to it. The `URL_EXTENSION`
pattern requires an extension to start with a letter, so `.2` is not one.

Expected slug: `docs/spec-v1.2` — unchanged from today.

Do not edit: integration tests assert exact bytes.
