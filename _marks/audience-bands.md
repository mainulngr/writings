---
status: living
date: 2026-10-15
---

# Audience Bands — age calibration for stories & books

The shared reference for the `story` and `picture-book` skills. `stories/` dir
names map to the **Band** column; a file's frontmatter `audience:` pins the
sub-band.

| Band | Ages | Reader | Words | Shape | Language |
|---|---|---|---|---|---|
| `children` — board | 0–3 | read aloud | 0–200 | one idea per page, rhyme/repetition, concrete nouns + sounds | very simple Bangla, short syllables |
| `children` — picture | 4–6 | read aloud | 300–800 | ~32pp / 12–14 spreads; page-turn tension; art carries half the story | musical read-aloud Bangla, gentle humour |
| `children` — early reader | 7–9 | reads alone | 1,000–2,500 | short chapters, one plotline, dialogue-heavy | clear Bangla, a few new words in context |
| `teens` | 10–17 | reads alone | 2,500–8,000+ | moral ambiguity allowed, faster pace, first person works | natural Bangla/English mix |
| `adult` | 18+ | reads alone | 800–3,000 (flash–short) | reflective, image-driven, open endings welcome | the voice in `_marks/voice.md` |

## Invariants across all bands

- The register stays gentle, warm, and unhurried — that is the signature, not
  a per-band variable. Adjust *complexity*, never warmth.
- Bangla-first; English loanwords only where natural to the audience.
- No preaching at any age — children included. Show the moment, let the
  reader take the meaning.
- For `children` work prefer concrete, sensory scenes (rain, animals,
  grandparents, food) over abstract emotion words.

## Frontmatter convention

Every `stories/` file and every book README carries:

```yaml
audience: children | teens | adult   # dir must match
sub: board | picture | early-reader  # children only
status: draft | polished | posted
```
