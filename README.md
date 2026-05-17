# Busy Mom Telegram Bot

A simple Telegram auto-reply bot for the `Busy Mom Daily Hacks` channel.

The bot can reply to:

- `/start`
- `/help`
- `/mom`
- `/checklist`
- `/kit`
- Plain text keywords: `MOM`, `MEAL`, `CLEAN`, `KIDS`, `MORNING`, `KIT`, `PRICE`

It is ready to deploy on Render as a Background Worker.

## Project Files

- `index.html` - Landing page
- `landing.css` - Landing page styles
- `LANDING_PAGE_SETUP.md` - Landing page hosting and link setup guide
- `render.yaml` - Render Blueprint configuration
- `requirements.txt` - Python dependency file
- `telegram-bot/bot.py` - Main Telegram bot
- `telegram-bot/README.md` - Detailed local and Render setup guide
- `telegram-bot/.env.example` - Example environment variables

## Do Not Upload Secrets

Do not commit or upload a real `.env` file.

Your real Telegram token should only be added in Render Environment Variables:

```text
TELEGRAM_BOT_TOKEN
CHANNEL_LINK
CHECKLIST_LINK
PAYMENT_LINK
```

## Quick Render Deploy

1. Create a new GitHub repository.
2. Upload these project files to the repository root.
3. Open Render.
4. Choose `New` then `Blueprint`.
5. Connect your GitHub repository.
6. Add the environment variables when Render asks.
7. Deploy.

When the worker is running, the logs should show:

```text
Busy Mom Helper bot is running. Press Ctrl+C to stop.
```

## Local Test

From PowerShell:

```powershell
cd C:\Users\Administrator\Documents\Codex\2026-05-15\tiktok\telegram-bot
.\start-bot.bat
```

Keep the terminal open while testing locally.

## Landing Page

The landing page is ready at `index.html`.

Before publishing, replace these placeholders in `index.html`:

```text
https://t.me/YOUR_BOT_USERNAME
https://YOUR_PAYMENT_LINK
```

For free hosting, use GitHub Pages:

1. Open the GitHub repo.
2. Go to `Settings`.
3. Go to `Pages`.
4. Source: `Deploy from a branch`.
5. Branch: `main`.
6. Folder: `/root`.
7. Save.
