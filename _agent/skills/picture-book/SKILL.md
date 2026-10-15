---
name: picture-book
description: >-
  Develop an illustrated children's book project — scaffold a book folder
  under books/, plan spreads, write per-spread text plus illustration
  briefs, inside age-band word budgets. Covers board book (0–3), picture
  book (4–6), and early reader (7–9). Triggers: "picture book", "illustrated
  book", "children's book", "chhotoder boi", "spread", "art brief".
allowed-tools:
  - read
  - write
  - edit
  - exec
  - grep
---

# Picture Book — project procedure

## Inputs to read first (always)

1. `_marks/audience-bands.md` — the children sub-bands carry the budgets:
   board (0–3): 0–200 words · picture (4–6): 300–800 words, ~32pp /
   12–14 spreads · early reader (7–9): 1,000–2,500, short chapters.
2. `_marks/voice.md` — warmth is invariant; complexity is the dial.

## Scaffold — one folder per book

```
books/<slug>/
  README.md      premise, audience frontmatter, spread plan, status
  spreads.md     per-spread text + illustration briefs
  art/           image refs, generated drafts, final art
```

README frontmatter: `audience: children`, `sub: board|picture|early-reader`,
`status: draft`.

## spreads.md format — one block per spread

```
## Spread N

**Text:**
<the words on the page — ≤2–3 short sentences for picture band>

**Illustration brief:**
Subject · composition · mood · palette · where the text sits
```

## Draft rules

- Text and art split the storytelling — never write what the picture shows.
- Page turns are the suspense engine; end each spread so the child wants
  the next one.
- Read-aloud test on every line: it must land well spoken, at bedtime pace.
- The art brief is a contract for an illustrator or image model — concrete
  subjects, lighting, and palette, no style-drift mid-book.
