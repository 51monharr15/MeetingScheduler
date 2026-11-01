# Agent restart note

**Repo:** https://github.com/51monharr15/MeetingScheduler (`main`)  
**Build:** see `VERSION`  
**UI truth:** `docs/UI-HIERARCHY.md`, `docs/UI-STYLE-GUIDE.md`

## Wrong place (do not use)

Meet work is **not** in `51monharr15/SIG-Stakeholder-Database` or `meet/` on branch `cursor/meet-scheduler-ca2b` (~1.6.x). That context mis-describes the app (e.g. “Records” tab and an **Attach** button). **This repo is the only source of truth.**

## Process

Discuss each fix with Simon until you agree. Simon must say to **authorise coding** before you change code.

**Reply style:** Keep outputs as short as possible. Simon will ask if he needs clarification. **One step at a time** — answer only the current topic; do not dump full lists or overload recall — **except** when he asks what you will change: then give the **complete** list for him to verify before coding.

**No coding while ambiguous.** Do not change code (or invent a design) when the requirement is unclear. Do not offer multiple-choice design menus (A / B / C): those are the agent’s guesses about what matters. Prefer what is already agreed in `docs/UI-STYLE-GUIDE.md` and `docs/UI-HIERARCHY.md`, and ask Simon only what you still cannot know.

**Principles are important.** Follow `docs/UI-STYLE-GUIDE.md`. Principles can conflict; if you would bend or compromise one, **discuss it with Simon first** — do not decide alone. Do not invent production banners, debug chrome, or layout redesigns to work around diagnosis — say the diagnosis in chat and wait for agreement.

**Deploy path:** Prefer putting authorised work on `main` so `git pull` works on Simon’s PC. Do not invent version numbers — ask.

## Naming

- **Sticky header** — whole top bar (title, actions, status strip, green nav)
- **Status strip** — grey meeting-status block

## Deploy (Simon)

Local: `D:\dev\MeetingScheduler`. Live: `git ftp push` (do not overwrite live `data/`). Hard-refresh after deploy (Ctrl+F5).

## Handoff

New agents: clone **this repo**, read this file first, then agree fixes with Simon before coding.
