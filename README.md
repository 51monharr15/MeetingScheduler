# Meet Scheduler

Self-contained meeting availability picker for Apache + PHP. **No database** — each meeting is stored as a human-readable plain-text file under `data/`.

Canonical repo: **https://github.com/51monharr15/MeetingScheduler**  
Local working copy: **`D:\dev\MeetingScheduler`**

## Quick start

1. Deploy this repo’s contents to your Apache web root (or a subdirectory such as `/meet/`).
2. Ensure PHP 8.1+ is enabled and `data/` is writable by the web server.
3. Visit the app URL to create a meeting. You receive a **random link** such as `/?=a7f3b2c91d04` (or `/meet/?=…` if deployed under `/meet/`) — save it; that code is the only way in.

```
/meet/?=a7f3b2c91d04
```

**Docs:** [docs/OPERATIONS.md](docs/OPERATIONS.md) (workflow & roles) · [LOCAL-TEST.md](LOCAL-TEST.md) · [UPDATING.md](UPDATING.md) · [GIT.md](GIT.md)

Meetings are not created by visiting a guessed URL. The slug is a random 12-character code. Internally each meeting also has a stable ID (e.g. `meet_a1b2c3d4e5f6`) in `data/aliases/{slug}.alias`.

## Features

- **Availability grid** — attendees pick time slots; times display in each user's local timezone
- **Suggestions** — highlights slots where others are already free (not limited to those slots)
- **Locations** — propose physical or video options; attendees mark preferences
- **Agenda & decisions** — plain-text lists editable by participants
- **Attachments** — URLs (recordings, transcript services) or pasted AI summary text
- **Recurrence** — weekly, monthly day (e.g. 19th), nth weekday (e.g. 3rd Monday), every N months, all Friday 13ths
- **Confirmation** — lock in a final slot and location

## File format

Meetings use the `@meet v1` plain-text format (see `lib/MeetFile.php`). Example sections:

- Header metadata (id, slug, title, date range, duration)
- `@@ recurrence`, `@@ agenda`, `@@ decisions`, `@@ locations`
- `@@ attachments`, `@@ attendees`, `@@ availability`, `@@ location_prefs`

Files live at `data/meets/{id}.meet`. Alias mapping at `data/aliases/{slug}.alias`.

## Apache notes

- `.htaccess` enables pretty URLs and blocks direct access to `data/`
- `data/.htaccess` denies all HTTP access to stored files
- Set directory permissions so PHP can write `data/meets/` and `data/aliases/`

## API

`POST api.php` with JSON body. Actions:

| Action | Purpose |
|--------|---------|
| `create` | Create meeting with slug, title, recurrence |
| `join` | Register attendee name/id |
| `save_availability` | Save selected ISO slot times |
| `add_location` | Propose a location |
| `save_location_prefs` | Attendee location preferences |
| `update_meta` | Agenda, decisions, settings, recurrence |
| `add_attachment` | URL or text attachment |
| `confirm` | Set confirmed slot/location |

`GET api.php?slug=...` returns the public meeting view.
