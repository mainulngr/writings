---
name: social-pipeline
description: >-
  Semi-automated social post production — the L2 loop: Mainul supplies
  seeds (keywords, context, a scene, a theme), the agent generates a batch
  of voice-checked candidates into the queue file, he sweeps them with
  keep/rework/drop verdicts, and approved pieces promote into dated social/
  files. Verdict history feeds future batches. Triggers: "batch",
  "generate posts", "queue", "sweep", "process verdicts", "post ideas",
  "explore these keywords".
allowed-tools:
  - read
  - write
  - edit
  - exec
  - grep
---

# Social Pipeline — the L2 loop

Two commands, one queue file: `social/_queue.md` (create on first use,
header `# Post Queue`).

## `batch` — seeds in, candidates out

1. **Read first, always:** `_marks/voice.md` for the register;
   `_marks/style-examples.md` for calibration; the tail of the queue for
   verdict history — what got `drop`ped or `rework`ed last time is what to
   do less of.
2. **Input = Mainul's seeds.** Keywords, context, a scene, a theme, a
   backlog line — he supplies the noticing, you do the shaping. One seed →
   1–3 candidates.
3. **No seeds given?** Offer candidates from `_starter/idea_backlog.md` or
   theme gaps in `social/` — propose, never push a blind batch.
4. **Shape each candidate** per the fb-post skill's structure: main caption
   + 2–3 styled-bg variants; Human Version only if the subject is raw.
   Run `voice-check` on each before enqueueing.
5. **Append to the queue** under a dated section:

```markdown
## YYYY-MM-DD · seed: "winter mornings, father's memory"

### 1 — Evening-slot candidate

<main caption>

**Variants:**
1. …
2. …

**Verdict:**
```

## `sweep` — verdicts in, promoted posts out

1. Read the queue. For each verdicted candidate:
   - `keep` → move into `social/YYYY_MM_DD.md` under the slot the
     `_marks/posting-schedule-bd.md` mark suggests for today; delete from
     queue.
   - `rework` (+ his note) → revise in place, re-mark `**Verdict:**
     reworked — recheck`.
   - `drop` → move to the queue's `## Dropped` tail with a one-line reason
     if known.
2. **Learnings** — tally patterns in drops/reworks. A repeated reason is a
   generation bias to fix; if it's a voice matter, it enters the
   voice-check feeding loop (a second occurrence → propose a `voice.md`
   edit).
3. **Report:** promoted / reworked / dropped counts + what the pattern says.

## Guards

- **Cadence:** warn if pending candidates exceed ~10 or a batch outruns
  the weekly slot budget (1–2/day).
- **Never auto-post.** Publishing is Mainul's manual step; profiles have
  no legitimate posting API.
- **Queue is transient.** Promoted and dropped entries don't linger —
  the queue trends toward empty, `social/` is the permanent record.
