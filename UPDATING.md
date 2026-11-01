# Updating Meet Scheduler

## FTP upload

**Preferred (this PC):** from `D:\dev\MeetingScheduler`:

```bat
git pull
git ftp push
```

git-ftp is configured for the live `/meet/` tree. `.git-ftp-ignore` keeps local `data/meets` and `data/aliases` off the server.

**Or FileZilla:**

1. `git pull` in your local MeetingScheduler clone (see [GIT.md](GIT.md)).
2. Upload the app files to your server’s Meet folder — including **new files** at the app root (see below).
3. Hard-refresh the browser (Ctrl+F5).

**Do not overwrite** `data/` on your server (your live meetings live there).

## FileZilla: refresh before upload

FileZilla caches the local folder listing. If you **right‑click a folder → Upload** after `git pull` added new files (e.g. `operations.php`, `favicon.svg`), those new files may **not** be in the upload queue — even though it looks as if you selected the whole folder.

**Before every upload:**

1. `git pull` first (so new files exist locally).
2. In FileZilla’s **local** pane, click the app folder (or press **F5** / View → Refresh) so the file list updates.
3. Confirm new files appear in the list (e.g. `operations.php`).
4. Then upload.

**Safer options:**

- Drag the **local app folder** onto the remote Meet folder (after refreshing the local pane).
- Or upload specific new files explicitly if you know what changed.
- After upload, check the **remote** pane: `operations.php` and `favicon.svg` should be present next to `index.php`.

This is a FileZilla behaviour, not a bug in Meet Scheduler — but it explains 404s when Git had a file your upload never included.

## New files (recent builds)

If you upload file-by-file, make sure these are on the server as well as the usual `assets/`, `lib/`, and `index.php`:

| File | Purpose |
|------|---------|
| `operations.php` | Opens the operations guide in the browser (reads `docs/OPERATIONS.md`) |
| `favicon.svg` | Calendar icon in the browser tab |
| `docs/OPERATIONS.md` | **Edit this** — the only copy of the guide text |

## Version check

The footer shows **Build x.y.z** (from `VERSION`).
