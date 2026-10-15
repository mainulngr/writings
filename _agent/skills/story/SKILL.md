---
name: story
description: >-
  Write a short story for this corpus across audience bands — children,
  teens, adult — Bangla-first fiction calibrated by the audience-bands mark.
  Covers band selection, drafting constraints, exemplar reference, and the
  stories/<band>/ file convention. Triggers: "write a story", "golpo",
  "children's story", "short fiction", "golpo lekho".
allowed-tools:
  - read
  - write
  - edit
  - exec
  - grep
---

# Story — drafting procedure

## Inputs to read first (always)

1. `_marks/audience-bands.md` — pick the band; it carries word budgets,
   reader mode (aloud vs alone), and per-band language rules.
2. `_marks/voice.md` — the register spine; warmth is invariant, only
   complexity changes per band.
3. Exemplar: `stories/adult/brishtir_opokkha.md` — the style benchmark for
   adult-band atmospheric fiction.

## Draft rules

- Band constraints beat instinct — check the table, not your guess, for
  length and vocabulary.
- Concrete sensory scenes over abstract emotion words; especially for
  children (rain, animals, grandparents, food).
- No preaching at any age. Show the moment; the reader takes the meaning.
- Bangla-first; English loanwords only where natural to the audience.

## Where it lands

- `stories/<band>/<slug>.md` — slug lowercase_underscored (a transliterated
  Bangla title like `brishtir_opokkha` is the established style).
- Frontmatter per the audience-bands mark:
  `audience: <band>` (+ `sub:` for children) and `status: draft`.

## After drafting

- Run `voice-check` — it audits both register and band fit.
- Read-aloud pass for `children` band: every sentence must work spoken.
- When a finished piece is approved, offer to canonize it into
  `_marks/style-examples.md` — the children/teens registers in `voice.md`
  are deliberately unsettled; real pieces are how they get earned.
