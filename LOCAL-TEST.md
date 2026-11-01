# Local test environment (PHP on your PC)

Use this to try changes before uploading via FTP.

## Prerequisites

- PHP 8.1+ installed (`php -v` in Command Prompt)
- This repo at `D:\dev\MeetingScheduler`

## Start the test server

```bat
cd /d D:\dev\MeetingScheduler
php -S localhost:8080
```

Leave that window open. The server runs until you press Ctrl+C.

## Open in browser

- Home: http://localhost:8080/
- Test meeting: http://localhost:8080/?my-test-meeting

## Where local data is stored

```text
D:\dev\MeetingScheduler\data\meets\
D:\dev\MeetingScheduler\data\aliases\
```

These are **only on your PC**. Do not overwrite live `data/` on the server.

## Testing after an update

1. Stop the server (Ctrl+C).
2. `cd /d D:\dev\MeetingScheduler` then `git pull`.
3. Start again:
   ```bat
   cd /d D:\dev\MeetingScheduler
   C:\php\php.exe -S localhost:8080
   ```
4. Hard-refresh the browser (Ctrl+F5).

## Differences from Apache

- Pretty URLs need Apache `mod_rewrite`. Locally use `http://localhost:8080/?slug-name`.
- Built-in PHP server is fine for development; production should stay on Apache.
