---
name: voice-check
description: >-
  Audit any draft in this corpus against the voice mark and audience bands —
  the shared final pass for fb-post, story, picture-book, and blog-post, or
  standalone review of an existing file. Reports violations with line refs
  and minimal fixes instead of rewriting. Triggers: "check this", "voice
  check", "does this sound like me", "review draft", "polish".
allowed-tools:
  - read
  - grep
  - edit
---

# Voice Check — audit procedure

`_marks/voice.md` is the source of truth. This checklist is the audit's
checkpoints — when the two disagree, the mark wins.

## Pass 1 — register (all content)

- **Subject choice** — মানুষ / লোকজন / আমরা, not finger-pointing আমি/তুমি
  (except deliberate Human Version / first-person pieces).
- **Hedged claims** — observations, not verdicts: মনে হয়, হয়তো, অনেকের
  ক্ষেত্রে, দেখা যায়.
- **Landing** — ends soft: hopeful note or innocent punchline. Never a
  burden.
- **The avoids list** — no personal attacks, no preachy imperatives, no
  cynical hopelessness, no attention-seeking drama, no "তোমরা সবাই"
  instructions.

## Pass 2 — channel fit

- **social/** — slot structure present (Main caption + styled-bg variants);
  variants genuinely 1–4 lines and self-contained.
- **stories/, books/** — band fit per `_marks/audience-bands.md`: word
  count in budget, vocabulary right for the reader, read-aloud quality for
  children.
- **blog/** — observes rather than instructs; ends on resonance.

## Output

- Short report: ✓/✗ per checkpoint with line references, then minimal
  suggested edits — smallest change that fixes the violation.
- Do not rewrite whole passages unless asked; Mainul keeps his sentences.
