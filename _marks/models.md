---
status: settled
---

# Model roles — Devin + Command Code rosters

*Dated 2026-10-15 — model rosters churn; re-derive when it matters.*

## The job split

Mainul curates the final prose — the model is the **editor, not the
ghostwriter**. What we buy: structure/plot guidance, improve–discard–add
critique, honest ratings, engagement reads. Conversations in English; the
story text is Bangla.

Consequence: comprehension > generation. Mid-tier models *read* Bangla far
better than they *write* it. The frontier edge shrinks but doesn't vanish —
weak Bangla comprehension misreads register (colloquial-warm → "simplistic").

## Roles → picks

| Job | Primary | Challenger |
|---|---|---|
| Editor/mentor (default) | `claude-sonnet-5-5` (CMD) | — |
| Deep critique / capstones | `claude-opus-5-5`, `claude-fable-5-1` | `gpt-6-astra` |
| Ops — sweeps, moves, brain chores | `swe` (Devin, current) | CMD free tiers, `deepseek-v4.1-flash-fast` |
| Cheap critique challenger | `deepseek-v4-pro` or `kimi-k3` | — |

Split rule: **by output language, not importance** — Bangla prose
generation → frontier; analysis, audit, housekeeping → cheap tier.

## Cost shape

- Writing tasks ≈ 5–15% of a coding session's tokens — context is small
  (voice.md + one mark + a seed).
- Bangla tokenizes ~3–8× costlier per word than English — the tax hits
  *output*, so drafting pays it; audits and analysis stay cheap.
- Realistic month (4 batches + sweep + 2 stories + audits + one course
  module): ~$3–8 on frontier, <$1 on cheap tiers.
- Reading exemplars is the expensive lane — read once, distill into
  `_study/short-fiction/device-catalog.md`, never re-read.

## Engagement reads — two layers

- **Attention mechanics** (hooks, open loops, pacing, payoff timing):
  reliable — well-documented craft knowledge.
- **This audience's taste on this platform**: hypothesis only — ground
  truth stays the reach-logging habit (`posting-schedule-bd.md`).
- **Drift risk**: attention patterns pull toward clickbait register → every
  engagement suggestion carries a **voice-cost** label (see `voice-check`
  critique mode). Declining a lift to protect register is a valid verdict.

## The A/B that settles it

Same existing story (`stories/adult/brishtir_opokkha.md`) through
`claude-sonnet-5-5` / `claude-opus-5-5` / `deepseek-v4-pro`-or-`kimi-k3` /
`swe` as control — identical brief: improve/discard/add + rating +
engagement read. Judge on: caught what's already known? saw what was
missed? rated honestly? Cheap to run — do it before committing to a tier.
