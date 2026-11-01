# Editing Meet Scheduler on your Windows PC

## Three copies of the code

| Copy | Where | Who updates it |
|------|--------|----------------|
| **1. Cloud Agent** | Cursor’s server (agent chat workspace) | The agent, or you if you edit there |
| **2. Your PC** | `D:\dev\MeetingScheduler` | `git pull` and your own edits |
| **3. Live website** | Your host via FileZilla | FTP upload from your PC |

These are **not the same folder**. Editing in the agent chat does not change files on your PC until code is pushed to GitHub and you `git pull` (or you edit the Windows files directly).

## Repo home

- GitHub: **https://github.com/51monharr15/MeetingScheduler**
- Local: **`D:\dev\MeetingScheduler`**

## Operations guide files

| File | What it is |
|------|------------|
| `docs/OPERATIONS.md` | The operations guide (edit this file only) |
| `operations.php` | Thin viewer: shows that Markdown in the browser |

## One-time: get up to date

```bash
cd /d/dev/MeetingScheduler
git fetch
git checkout main
git pull
ls index.php operations.php favicon.svg docs/OPERATIONS.md
cat VERSION
```

You should see build **1.8.53** (or newer) in `VERSION`.

## Edit on your PC

1. In Cursor, open **`D:\dev\MeetingScheduler`**.
2. Edit and Save.
3. Refresh the browser pointed at that same folder.

## Save to Git

```bash
cd /d/dev/MeetingScheduler
git status
git add index.php
git commit -m "Wording change on home page"
git push
```
