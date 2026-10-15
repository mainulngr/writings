---
status: promoted
promoted: _agent/skills/social-pipeline/
date: 2026-10-15
---

# Social pipeline — semi-automated idea generation + review loop

The question: how to generate post ideas semi-automatically — agent drafts
candidates, Mainul reviews with a verdict, approved ones flow into the
posting pipeline.

## The honest ceiling first

Automation can **shape**, it can't **notice**. The best posts in this
corpus come from real observation (the tubewell post worked because a real
event met real claustrophobia). Pure-LLM idea generation trends generic.
So the design keeps a place for his 10-second seed — expect seeds to
outperform generated ideas.

## Automation levels

- **L1 — prompt-assisted** (exists today): he gives a topic, `fb-post`
  drafts, he edits, posts. This is the floor, not the goal.
- **L2 — batch + verdict queue** (the sweet spot): on demand, the agent
  generates a batch of candidates into a queue file; he sweeps with
  verdicts; approved ones land in dated files; reach gets logged.
- **L3 — scheduled autonomy** (cron-drafted batches): solves a problem
  that doesn't exist — drafts wait for review anyway. On-demand batching
  gives the same output with his control intact.
- **L4 — auto-publish**: possible only for Pages (Meta Graph API; app +
  token setup). Personal profiles have no official API — auto-posters are
  ToS-violating. Defer; if a page lane matures, scheduling becomes real.

## Where ideas come from (generation sources)

- **Backlog expansion** — `_starter/idea_backlog.md` one-liners → posts.
- **Theme coverage** — `voice.md`'s 10-theme checklist vs `social/`
  history: rotate toward underused themes, avoid repeats.
- **Seasonal/situational hooks** — BD calendar: monsoon, winter mornings,
  Ramadan/Eid, exam season, load shedding, cricket. Calendar-driven
  prompts are cheap and reliably relevant.
- **Seed prompts** — the agent asks ("what did you notice today? what
  gently annoyed you this week?"), he answers one line, agent expands.
- **Verdict history** — the queue's keep/rework/drop record tells the next
  batch what to do more/less of. The loop learns his taste.

## The mechanism (if built)

- **One rolling queue file** — drafts land there dated + numbered, each
  with a verdict marker (`keep` / `rework` / `drop`). His review = editing
  the file; zero tooling, zero new UI.
- **Promotion** — `keep` pieces move into `social/YYYY_MM_DD.md` slot
  sections (existing convention, unchanged).
- **Voice-check stays in the loop** — every candidate audited before it
  reaches him; verdicts feed both the voice rules and the generation
  sources.
- **Cadence guard** — batch sized to the schedule (1–2 slots/day → weekly
  batch of ~6–8). Bigger queues rot.

## Working lean — decided 2026-10-15

L2 confirmed by Mainul, with a refinement that made it better: **seeds are
the primary input.** He supplies context/keywords he wants explored; the
agent shapes. Generated-without-seed batches are secondary — offered from
backlog/theme gaps, never pushed blind.

Built as the `social-pipeline` skill: `batch` (seeds → voice-checked
candidates → queue) + `sweep` (verdicts → promote/rework/drop + learnings).
Queue home decided: one rolling `social/_queue.md`, dated batch sections.
L4 revisits only if a page lane matures.

## Open sub-questions

- Who writes seeds vs generated — and do we measure which performs?
- Does Onkur Notes / mainulsq change what the pipeline feeds (lane-aware
  generation)?
