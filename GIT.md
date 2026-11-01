# Git — MeetingScheduler

Canonical repo: **https://github.com/51monharr15/MeetingScheduler**

Local working copy: **`D:\dev\MeetingScheduler`**

## Clone

```bat
cd /d D:\dev
git clone https://github.com/51monharr15/MeetingScheduler.git
```

`index.php`, `api.php`, `VERSION`, `assets/`, `lib/`, `data/`, and docs live at the **repo root**.

## Get the latest code

```bat
cd /d D:\dev\MeetingScheduler
git checkout main
git pull
```

## What to upload to your web server

Upload the app tree so the live Meet URL (often `/meet/`) contains `index.php`, `api.php`, `assets/`, `lib/`, `data/`, etc. See [UPDATING.md](UPDATING.md).

## Key files

| File | What it is |
|------|------------|
| `index.php` | Home page (“Find my meetings”, create meeting) |
| `operations.php` | Operations guide (footer link) |
| `favicon.svg` | Browser tab icon |
| `api.php` | Server API |
| `VERSION` | Build number in footer |

UI wording on the home page is in `index.php`. Most in-app labels are in `assets/js/app.js`.
