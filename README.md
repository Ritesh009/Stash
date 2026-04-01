# 📦 Stash

> A place that doesn’t know you. And never will.

Stash is a privacy-first bookmarking app that runs entirely in your browser. No account, no server, no subscription. Your data never leaves your device.

→ **[Open Stash](https://ritesh009.github.io/Stash/)**

-----

## What Stash is

You can’t stop someone seeing you walk into a library. But what you read, what you underline, what you take notes on — that can be yours alone.

The web works the same way. The moment you search for something, that’s already visible. Stash can’t change that. What it can do is protect everything that comes after — what you chose to keep, what you annotated, what you came back to, the pattern of what matters to you. That layer is genuinely private, and that’s where Stash lives.

In a world where everything knows you, Stash doesn’t. That’s not a small thing.

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

When you first open Stash you set a passphrase. This does two things:

1. **Derives storage key names** — the names of the storage keys themselves are a SHA-256 hash of your passphrase. Nothing in storage is named “stash” or “items”. Without your passphrase you can’t even find the data, let alone read it.
1. **Derives the AES-256 encryption key** — all data is encrypted using PBKDF2 (200,000 iterations). Without your passphrase the data is unreadable.

Data is stored in two places, both encrypted:

- **OPFS** (primary) — a private file system managed by the browser on your device
- **localStorage** (shadow) — an encrypted fallback under the derived key name

Your passphrase is never stored anywhere. You can verify your storage status in **⚙️ Settings → Security**.

**Lock policy:** Stays unlocked for 24 hours or until you close the tab. Lock manually anytime via Settings → Lock Stash.

**Forgot your passphrase?** Settings → Danger Zone → Export backup & reset. Stash auto-exports an unencrypted backup, wipes all encrypted data, and lets you start fresh. Import the backup, then delete the file from Files — it is unencrypted.

**What Stash doesn’t protect:** The act of searching or browsing is visible to whoever handles your internet traffic. Stash protects what you keep — not how you found it.

> Requires HTTPS — use via GitHub Pages or your own HTTPS host. `crypto.subtle` is not available on plain HTTP.

-----

## Install

**iPhone** — Open in Safari → Share → Add to Home Screen

**Android** — Open in Chrome → ⋮ → Add to Home Screen

**Desktop** — Just open the URL in any browser, no install needed

> ⚠️ On iPhone, use Stash in **Safari** (not the home screen icon) for Stash Clip to work. iOS keeps browser storage and home screen app storage completely separate.

-----

## Stash Clip

Save any page with one tap. Go to the **🔖 Clip** tab in Stash, copy the bookmarklet code, and add it as a bookmark in your browser. Works in Safari, Chrome, Firefox and Edge.

When Stash is open in another tab, clips are saved silently without asking for your passphrase again. If no tab is open, you’ll be asked to unlock first — your data is worth the extra second.

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

Move data between devices via **Share → Export** on one device and **Share → Restore** on the other.

-----

## License

MIT — free to use, modify and self-host.