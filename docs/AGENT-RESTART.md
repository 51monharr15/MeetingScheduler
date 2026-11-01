# Agent restart note

**Repo:** https://github.com/51monharr15/MeetingScheduler (`main`)  
**Build:** see `VERSION`  
**UI truth:** `docs/UI-HIERARCHY.md`, `docs/UI-STYLE-GUIDE.md`

## Wrong place (do not use)

Meet work is **not** in `51monharr15/SIG-Stakeholder-Database` or `meet/` on branch `cursor/meet-scheduler-ca2b` (~1.6.x). That context mis-describes the app (e.g. “Records” tab and an **Attach** button). **This repo is the only source of truth.**

## Process

Discuss each fix with Simon until you agree. Simon must say to **authorise coding** before you change code.

**Reply style:** Keep outputs as short as possible. Simon will ask if he needs clarification. **One step at a time** — answer only the current topic; do not dump full lists or overload recall.

**No coding while ambiguous.** Do not change code (or invent a design) when the requirement is unclear. Do not offer multiple-choice design menus (A / B / C): those are the agent’s guesses about what matters. Prefer what is already agreed in `docs/UI-STYLE-GUIDE.md` and `docs/UI-HIERARCHY.md`, and ask Simon only what you still cannot know.

## Faults Simon reported (2026-11-01)

Agreed and implemented on the UX-fixes branch (verify in review):

1. **Attachments** — **Add** / **Save** on rows (blur-save kept as fallback).
2. **Locations** — same (**Add** on new row; **Save** on existing).
3. **Notes Saves** — closed; not a real problem (Attachments was).
4. **Top header** — Help + Copy always visible (stacked); status block shows Signed in + Status + time, then location, then expandable description / agenda·decisions·attachments·notes; no **More ▾**.
5. **Getting started next-step hints** — suggest Getting started or next setup step (no auto-jump).
6. **Mobile calendar copy** — tap/click wording; toolbar Save/Copy line; **Invert selection** button rename.
7. **Button padding** — reduced (~half vertical; slightly less than half horizontal).

## Deploy (Simon)

Local: `D:\dev\MeetingScheduler`. Live: `git ftp push` (do not overwrite live `data/`).

## Handoff

New agents: clone **this repo**, read this file first, then agree fixes with Simon before coding.
