# Editing Meet Scheduler on your Windows PC

## Three copies of the code (important)

| Copy | Where | Who updates it |
|------|--------|----------------|
| **1. Cloud Agent** | Cursor’s server (the workspace in the agent chat) | The agent, or you if you edit there |
| **2. Your PC** | Your `git clone` of **MeetingScheduler** on Windows | `git pull` and your own edits |
| **3. Live website** | Your host via FileZilla | FTP upload from your PC |

These are **not the same folder**. Editing in the agent chat does **not** change files on your PC or your localhost until code is **pushed to GitHub** and you **`git pull`** on Windows (or you edit the Windows files directly).

## Repo home

Canonical GitHub repo: **https://github.com/51monharr15/MeetingScheduler**

Do **not** put Meet Scheduler work in `SIG-Stakeholder-Database`. That repo is only for Stroke Improvement Group stakeholder database work.

## Two different “operations” files

| File | What it is |
|------|------------|
| `docs/OPERATIONS.md` | **The** operations guide (edit this file only) |
| `operations.php` | Thin viewer: shows that Markdown in the browser |

## One-time: get fully up to date on Windows

Open **Git Bash**, go to your clone (change the path to yours):

```bash
cd /c/Users/YOURNAME/MeetingScheduler
git fetch
git checkout main
git pull
```

Check these exist:

```bash
ls index.php operations.php favicon.svg docs/OPERATIONS.md
cat VERSION
```

You should see build **1.8.53** (or newer) in `VERSION`.

## Edit on your PC (so localhost F5 works)

1. In Cursor, open the folder **`MeetingScheduler`** on your **Windows disk** (File → Open Folder).
2. Edit e.g. `index.php` and **Save**.
3. Refresh the browser that points at **that same folder** (your local PHP server / XAMPP / etc.).

If localhost still shows old text, your web server is serving a **different directory** — find which folder Apache/PHP uses and edit that one, or copy files there.

## After you edit: save to Git

In Git Bash, in your clone folder:

```bash
cd /c/Users/YOURNAME/MeetingScheduler
git status
git add index.php
git commit -m "Wording change on home page"
git push
```
