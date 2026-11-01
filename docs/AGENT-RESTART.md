# Agent restart note

**Repo:** https://github.com/51monharr15/MeetingScheduler (`main`)  
**Build:** see `VERSION` (1.8.53 when this note was added)  
**UI truth:** `docs/UI-HIERARCHY.md`, `docs/UI-STYLE-GUIDE.md`

## Wrong place (do not use)

Meet work is **not** in `51monharr15/SIG-Stakeholder-Database` or `meet/` on branch `cursor/meet-scheduler-ca2b` (~1.6.x). That context mis-describes the app (e.g. “Records” tab and an **Attach** button). **This repo is the only source of truth.**

## Process

Discuss each fix with Simon until you agree. Simon must say to **authorise coding** before you change code. Keep replies short when he is on mobile.

## Faults Simon reported (2026-11-01) — not yet fixed

1. **Meeting Resources → Attachments (amber/yellow table):** Rows save when focus leaves the field (desktop **Tab**). There is **no Save button**. On mobile there is **no Tab**, so he often **cannot save or add** rows.

2. **Same pattern may apply** to the **Locations** table (also saves on leaving a field).

3. **Notes / other blocks on Meeting Resources** use a **Save** button at the bottom; on mobile that may still be hard to reach (keyboard, scrolling).

4. **Top header:** On a narrow screen too much is hidden behind **More ▾**; the nav does not say **Notes** (only **Meeting Resources**).

5. **Getting started:** He wants a clearer way back to instructions between steps (tab exists; UX TBD).

6. **Mobile calendar:** Help text talks about **drag**; on phone you **tap** slots. Wording/fix TBD.

## Deploy (Simon)

Local: `D:\dev\MeetingScheduler`. Live: `git ftp push` (do not overwrite live `data/`).

## Handoff

New agents: clone **this repo**, read this file first, then agree fixes with Simon before coding.
