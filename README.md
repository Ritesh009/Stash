# 📦 Stash

> A place that doesn’t know you. And never will.

Stash is a privacy-first bookmarking app that runs entirely in your browser. No account, no server, no subscription. Your data never leaves your device.

→ **[Open Stash](https://ritesh009.github.io/Stash/)**

-----

## Features

**Saving**

- Save web pages, notes, ideas and links
- Stash Clip — one-tap saving from any browser via a bookmarklet
- Duplicate detection on save — merge, replace or keep both

**Organising**

- Tags with instant filter, search across titles, URLs, descriptions and tags
- Sort by newest, oldest, A–Z, Z–A
- Date groups — Today, Yesterday, This Week, This Month

**Managing**

- Swipe left to delete, swipe right to edit
- Bulk delete, find & resolve duplicates
- Trash with 30-day recovery and 5-second undo

**Data**

- Import browser bookmarks (Chrome, Safari, Firefox, Edge) — folders become tags
- Export / Restore as JSON — merge or full replace
- Daily backup prompt + shadow backup for data safety

-----

## Privacy & Security

- **No server** — data stored locally on your device, never transmitted
- **No tracking** — zero analytics, no third-party scripts
- **No Google** — system fonts, favicons via DuckDuckGo
- **No account** — nothing to sign up for

**How data is stored:**

Every time you open Stash for the first time, you set a passphrase. This is used for two things:

1. **Deriving storage key names** — the names of the storage keys themselves are a SHA-256 hash of your passphrase. An extension scanning localStorage or OPFS cannot find your data without knowing your passphrase — there is nothing named “stash” or “items” to look for.
1. **Deriving the AES-256 encryption key** — all data is encrypted using PBKDF2 (200,000 iterations) with your passphrase and a random salt. Without your passphrase the data is unreadable.

Data is stored in two places, both encrypted:

- **OPFS** (primary) — a private file system managed by the browser on your device
- **localStorage** (shadow) — an encrypted fallback under the derived key name

Your passphrase is never stored anywhere. You can verify your storage status in **⚙️ Settings → Security**.

**Lock policy:** Stash stays unlocked for 24 hours or until you close the tab — whichever comes first. You can also lock manually via Settings → Lock Stash.

**Forgot your passphrase?** Go to Settings → Danger Zone → Export backup & reset. Stash will auto-export an unencrypted backup to Files, wipe all encrypted data, and let you set a new passphrase. Import the backup to restore your items — then delete the backup file from Files as it is unencrypted.

> ⚠️ This encryption protects against extension snooping and casual device access. It does not protect against someone who has your unlocked device and knows your passphrase.

-----

## Install

**iPhone** — Open in Safari → Share → Add to Home Screen

**Android** — Open in Chrome → ⋮ → Add to Home Screen

**Desktop** — Just open the URL in any browser, no install needed

> ⚠️ On iPhone, use Stash in **Safari** (not the home screen icon) for Stash Clip to work. iOS keeps browser storage and home screen app storage completely separate.

-----

## Stash Clip

Save any page with one tap. Go to the **🔖 Clip** tab in Stash, copy the bookmarklet code, and add it as a bookmark in your browser. Works in Safari, Chrome, Firefox and Edge.

-----

## Self-hosting

Stash is a single HTML file — no build step, no dependencies.

1. [Fork this repo](https://github.com/ritesh009/Stash/fork)
1. Go to **Settings → Pages → Deploy from branch → main**
1. Your Stash is live at `https://YOUR-USERNAME.github.io/Stash/`

Free forever on GitHub Pages.

-----

## Why no sync?

Stash is local-first by design. Firebase contradicts the privacy philosophy, and iOS makes serverless sync technically impossible — Safari and the home screen PWA use separate storage with no bridge.

Use Stash in Safari for the best experience. Move data between devices via **Share → Export** on one device and **Share → Restore** on the other.

-----

## License

MIT — free to use, modify and self-host.