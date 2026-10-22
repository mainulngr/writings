---
description: "project core"
trigger: always_on
---

# writings — Core

## Project

- **What:** Mainul's personal writing corpus — Bangla-first social posts,
  fiction across age bands, illustrated children's books, and blog essays.
  Content repo, not code; no build, no tests.
- **Remote:** github.com/mainulngr/writings (origin, main)
- **Docs:** `_marks/` (durable reference + decisions)
- **Agent memory:** `_journal/` — handoff + changes/ (in-flight work) + archive/ (done/dropped)
- **Skills:** `_agent/skills/` — `fb-post`, `story`, `picture-book`,
  `blog-post`, `voice-check` (shared audit; always the last pass),
  `social-pipeline` (seed → batch → verdict → promote loop)

## Layout — one dir per channel

- `social/` — FB posts; one file per day (`YYYY_MM_DD` name), `## Morning|Evening|Night` slots → `### Main caption` + `### Short variants (styled background)` + optional `### Human Version`. `social/_queue.md` = the pipeline's rolling draft queue.
- `blog/` — long-form essays, one file per post.
- `stories/<children|teens|adult>/` — fiction by audience band (`_marks/audience-bands.md` carries budgets + frontmatter convention).
- `books/<slug>/` — one folder per illustrated book (README · spreads.md · art/).
- `_warehouse/assets/` — media library (img/audio/video used in posts), gitignored staging, unversioned; `Makefile` inside holds one-off ffmpeg snippets. Permanent home undecided (see handoff).
- `_starter/idea_backlog.md` — idea capture, one line per idea.
- `_study/` — research subjects (`short-fiction/` = niche scan + course).
- `data` → symlink to `/mega/mountain/writings/` — corpora, teardown
  artifacts, derived catalogs (own git inside; educational reference only).

## Key marks

- `_marks/voice.md` — **the voice contract**: persona, tone, structure, AI guidelines. Read before drafting anything.
- `_marks/audience-bands.md` — age calibration table (board|picture|early-reader, teens, adult).
- `_marks/style-examples.md` — reference posts for calibration.
- `_marks/posting-schedule-bd.md` — posting windows, BD audience (UTC+6).
- `_marks/models.md` — model role picks across Devin + Command Code
  rosters (editor-not-ghostwriter split; dated — rosters churn).
- `_marks/production.md` — how a children's piece becomes a published book;
  points at the onkurreads product marks (shelf, audio/art, rights).

## Conventions

- Language: Bangla first, light natural English; follow `voice.md` over generic style.
- New post day → new dated file in `social/`; never backfill another day's file.
- Cores carry pointers, not paragraphs — depth belongs in `_marks/`.
