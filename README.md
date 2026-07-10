# Offline Activation — Telegram Mini App

Single-file prototype (`index.html`) — no build step, no dependencies to install.

## Deploy with GitHub Pages (free HTTPS hosting)

1. Create a new GitHub repository and upload `index.html` to its root (file name must stay `index.html`).
2. In the repo: **Settings → Pages → Source** → select the `main` branch, folder `/ (root)` → **Save**.
3. Wait ~1 minute — GitHub will give you a URL like:
   `https://your-username.github.io/your-repo-name/`
4. Open **@BotFather** in Telegram → your bot → `/newapp` (or **Bot Settings → Menu Button** to edit an existing one) → paste that URL as the **Web App URL**.

Your Mini App is now live in Telegram.

## Notes

- Everything runs client-side (mock backend, mock payments) — see the comments at the top of the `<script>` block in `index.html` for exactly where to plug in a real server, Telegram Stars invoices, and other payment providers.
- Admin panel access is restricted by Telegram username inside `CONFIG.adminUsernames` — edit that list before going live.
- Re-upload `index.html` any time you want to update the live app; GitHub Pages redeploys automatically within a minute or two.
