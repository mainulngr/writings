---
status: settled
---

# Model roles — Devin + Command Code rosters

*Dated 2026-10-15 — model rosters churn; re-derive when it matters.*

## The job split

Mainul curates the final prose — and the model is a **co-author, not only
an editor** (amended 2026-10-15): authorized to draft in his voice when he
asks, to "write the words he would have written had the 2012→now
continuity been real". The counterfactual writer is an approximation —
it lives in `voice.md` + `style-examples.md` + the corpus itself, and the
correction/verdict loop tightens it. What we buy: drafts he can own,
structure/plot guidance, improve–discard–add critique, honest ratings,
engagement reads. Conversations in English; the story text is Bangla.

Consequence: comprehension > generation. Mid-tier models *read* Bangla far
better than they *write* it. The frontier edge shrinks but doesn't vanish —
weak Bangla comprehension misreads register (colloquial-warm → "simplistic").

**Refinement (same day):** stories get *shaped* in English too — beats,
structure, plot discussion — and Mainul authors the Bangla prose himself
(see the `story` skill's two-phase workflow). That removes Bangla
generation from the model's job entirely; the English artifact stays at
blueprint level so the Bangla version is re-authored, not translated. The
only Bangla-dependent task left is critiquing the finished text.

## Roles → picks

| Job | Primary | Challenger |
|---|---|---|
| Editor/mentor (default) | `claude-sonnet-5-5` (CMD) | — |
| Deep critique / capstones | `claude-opus-5-5`, `claude-fable-5-1` | `gpt-6-astra` |
| Ops — sweeps, moves, brain chores | `swe` (Devin) | CMD free tiers, `deepseek-v4.1-flash-fast` |
| Cheap critique challenger | `deepseek-v4-pro` or `kimi-k3` | — |
| Co-drafting (Bangla prose, on request) | `claude-opus-5-5` (Devin) | `gemini-4-argon`, `gpt-6-astra` |

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

**Attribution convention:** when a model-drafted version lands in a corpus
file, label it with the model id — `## Suggested rewrite (Devin ·
claude-opus-5-5-medium)` — so parallel A/B versions stay attributable.
Verify the running model before labeling (the session's own model, not
an assumed default) — the baseline's first label was wrong and corrected.

## First evidence (2026-10-15 — `_baseline.md` six-way)

Same brief, six versions landed. Observed, not assumed:

- **opus-5-5**: added emotional material — new images (the house growing
  when siblings leave, son's hands gripping the shirt), a lightened-ending
  reframe. The only version that behaved as co-author. Register drifts
  slightly more polished-literary than his — lift the beats, not the text.
- **sonnet-5-5**: faithful clean edit, fixed geography/seam; over-stated
  the reveal. Adds clarity.
- **gemini-4-argon**: decent texture but register tilts bookish
  (বালিয়াড়ি, মনের গহীনে) vs his conversational calm. Adds texture.
- **deepseek-v4-pro**: reshaped the frame (reverie opening), clean seam
  fix; stayed inside the given structure. Rearranges.
- **kimi-k3**: near-verbatim copyedit — fixed typos, engaged nothing.
  Polishes.
- The "Suggested rewrite" in the file is also opus-5-5 (this session),
  but under a *minimal-edit* brief — so the two opus versions show the
  same model under two briefs, not two models. Brief shapes the output
  as much as model choice does.
- Pattern: **open models polish or rearrange; frontier models add.** At
  this task, on this evidence: opus-5-5 ≈ $0.05/piece, and earns it.
- CMD note: Claude ids are plan-gated there (sonnet needs GOAT+, opus
  Provider+) — Devin's roster carries them fine headless.

## The A/B that settles it

Same existing story (`stories/adult/brishtir_opokkha.md`) through
`claude-sonnet-5-5` / `claude-opus-5-5` / `deepseek-v4-pro`-or-`kimi-k3` /
`swe` as control — identical brief: improve/discard/add + rating +
engagement read. Judge on: caught what's already known? saw what was
missed? rated honestly? Cheap to run — do it before committing to a tier.
