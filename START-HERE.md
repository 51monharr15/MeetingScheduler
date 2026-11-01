# Start here — Meet Scheduler

**Working copy:** `D:\dev\MeetingScheduler`  
**GitHub:** https://github.com/51monharr15/MeetingScheduler (`main`)  
**Build:** see `VERSION`

## Develop locally

```bat
cd /d D:\dev\MeetingScheduler
git pull
php -S localhost:8080
```

Open http://localhost:8080/

## Key paths

| Path | Purpose |
|------|---------|
| `index.php` / `api.php` / `assets/` / `lib/` | App |
| `data/` | Local meetings only (not in git; do not overwrite live `data/`) |
| `docs/OPERATIONS.md` | Operations guide (shown via `operations.php`) |
| `docs/UI-HIERARCHY.md` | Current UI hierarchy / wording reference |
| `docs/UI-STYLE-GUIDE.md` | UI principles |
| `LOCAL-TEST.md` | Local PHP server detail |
| `EDITING.md` | Edit / commit workflow |
| `GIT.md` | Clone / pull |
| `UPDATING.md` | Deploy to live |

## Deploy to live

From this folder (git-ftp is configured locally):

```bat
cd /d D:\dev\MeetingScheduler
git ftp push
```

Uploads the app root to the live `/meet/` tree. Does not upload `data/meets` or `data/aliases` (see `.git-ftp-ignore`).
