---
name: fb-post
description: >-
  Draft a Facebook/social post for this corpus — Bangla-first reflective
  captions with styled-background variants and an optional raw "Human
  Version". Covers slot choice via the BD posting schedule, the dated file
  convention in social/, and post-publish reach logging. Triggers: "write a
  post", "fb caption", "ajker post", "evening post", "styled background".
allowed-tools:
  - read
  - write
  - edit
  - exec
  - grep
---

# FB Post — drafting procedure

## Inputs to read first (always)

1. `_marks/voice.md` — the voice contract. Non-negotiable.
2. `_marks/style-examples.md` — skim 2–3 entries for calibration.
3. `_marks/posting-schedule-bd.md` — pick the slot (Morning/Evening/Night)
   for today's weekday in UTC+6.
4. `_starter/idea_backlog.md` — if Mainul hasn't given a topic, offer one
   from the backlog.

## Where it lands

- File: `social/YYYY_MM_DD.md` — create if absent, header `# Posts – DD-MM-YYYY`.
- Section: `## <Slot>` (Morning | Evening | Night). Never backfill another day.

## Draft shape (inside the slot section)

1. `### Main caption` — relatable scene → 2–4 short reflections → gentle
   takeaway → soft punchline so readers leave smiling, not burdened.
2. `### Short variants (styled background)` — 2–3 options, 1–4 lines each,
   self-contained enough for FB's colored-background cards.
3. `### Human Version` — optional; only when the post is meant as personal
   confession. First person, diary-like, spoken register.

## After drafting

- Run the `voice-check` skill on the draft before showing it.
- After Mainul posts it: append time posted + rough reach to the slot
  section — that log is what tunes the schedule mark over time.
- If a published piece feels right to him, offer to canonize it into
  `_marks/style-examples.md` — exemplars are how voice rules get earned.
