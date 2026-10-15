---
name: blog-post
description: >-
  Write a long-form blog post for this corpus — outline-first drafting in
  the same reflective register as the voice mark but essay-length and
  structured with headings. Covers topic shaping, draft passes, and the
  blog/ file convention. Triggers: "blog post", "article", "essay",
  "long-form", "blog lekho".
allowed-tools:
  - read
  - write
  - edit
  - exec
  - grep
---

# Blog Post — drafting procedure

## Inputs to read first (always)

1. `_marks/voice.md` — the register spine. Blog drops the FB punchline
   requirement; the worldview and humility stay.
2. `_starter/idea_backlog.md` — if no topic given, offer candidates.

## Shape

1. **Angle first** — one sentence: what this piece notices that the reader
   hasn't named yet. If it can't be said in one line, the post isn't ready.
2. **Outline** — 3–6 sections, each one move of the argument, sketched as
   bullets before prose.
3. **Draft** — Bangla-first (light English where natural); headings allowed;
   paragraphs longer than FB but sentences stay short and clear.
4. **Tighten** — cut the warm-up paragraph if the piece truly starts later;
   end on resonance, not summary.

## Where it lands

- `blog/<slug>.md`, frontmatter:

```yaml
---
title: "…"
date: YYYY-MM-DD
status: draft | published
---
```

## After drafting

- Run `voice-check`. Blog-specific extra: no lecture voice — observe,
  don't instruct.
- If a published piece lands well, offer to canonize it into
  `_marks/style-examples.md`.
