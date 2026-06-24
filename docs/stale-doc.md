---
title: "Stale Document"
owner: "platform"
status: "current"
last_reviewed: "2020-01-01"
kb-locked: false
tags:
  - fixture
  - staleness
---

# Stale Document

Fixture for staleness integration tests. The last_reviewed date is far in the past so
computeStaleness always returns "stale" regardless of when the test runs.

Do not edit: tests assert last_reviewed and staleness state for this fixture.
