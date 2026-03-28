# 📦 Stash

> Your personal archive. Stored on your device, free forever.

Stash is a lightweight, privacy-first bookmarking and note-saving app that runs entirely in your browser. No account. No server. No subscription. Your data never leaves your device.

-----

## ✨ Features

- **Save anything** — web pages, notes, ideas, links
- **Safari Clip** — one-tap saving from any page in Safari via a bookmarklet
- **Tags & search** — organize and find items instantly
- **Edit items** — tap any card to edit title, tags, and description
- **Date groups** — items grouped by Today, Yesterday, This Week, This Month
- **Swipe to delete** — swipe left on any card to remove it
- **Import / Export** — your data as JSON, fully portable
- **Daily backup** — prompted every 24hrs to save a backup file to your device
- **Shadow backup** — automatic localStorage copy, auto-restores if data is lost
- **Duplicate detection** — merge, replace, or keep both when saving duplicates
- **Works offline** — service worker caches the app for offline use
- **Installable on iPhone** — add to home screen via Safari

-----

## 🔒 Privacy

Stash is designed to be private by default:

- **No server** — all data stored in your browser’s localStorage
- **No analytics** — zero tracking, no third-party scripts
- **No Google** — fonts are system fonts, favicons fetched via DuckDuckGo
- **No account required** — nothing to sign up for or log in to
- **Your data is yours** — export as JSON anytime, no lock-in

-----

## 📱 Install on iPhone

1. Open your Stash URL in **Safari**
1. Tap the **Share button** (↑) at the bottom
1. Tap **“Add to Home Screen”**
1. Tap **Add**

Stash will appear as an app icon on your home screen and open fullscreen.

> ⚠️ **Important:** Use Stash in Safari (not the home screen icon) if you want Safari Clip to work. iOS stores data separately for each context.

-----

## 🔖 Safari Clip Setup

Safari Clip lets you save any page to Stash with one tap while browsing.

1. Go to the **🔖 Safari Clip** tab inside Stash
1. Tap **Copy Code** to copy the bookmarklet
1. In Safari, bookmark any page — name it **“Stash It”**
1. Edit that bookmark and replace the URL with the copied code
1. Done — tap “Stash It” from any page to save it instantly

-----

## 💾 Backup & Data Safety

Stash uses two layers of backup:

**Layer 1 — Shadow copy**
Every save writes a second copy to a separate localStorage key. If iOS clears your main data, Stash silently restores from this copy on next open.

**Layer 2 — Daily file backup**
Every 24hrs, a green banner appears prompting you to save a dated JSON file (e.g. `stash-backup-2026-03-28.json`) to your iPhone’s Files app. This survives browser storage clears.

You can also manually export anytime via **Share → Export**.

-----

## 🛠 Self-Hosting

Stash is a single HTML file. No build step, no dependencies.

1. Download `index.html`
1. Host it anywhere — [GitHub Pages](https://pages.github.com), [Netlify Drop](https://app.netlify.com/drop), or any static host
1. Open the URL in Safari on your iPhone

**GitHub Pages (recommended):**

- Create a repo, upload `index.html`, enable Pages under Settings → Pages
- Your app will be live at `https://YOUR-USERNAME.github.io/REPO-NAME/`

-----

## 🗺 Roadmap

|Feature                                     |Status   |
|--------------------------------------------|---------|
|Save notes & web pages                      |✅ Done   |
|Tags, search, sort, filter                  |✅ Done   |
|Safari Clip bookmarklet                     |✅ Done   |
|Edit items                                  |✅ Done   |
|Import / Export                             |✅ Done   |
|Duplicate detection                         |✅ Done   |
|Daily backup prompts                        |✅ Done   |
|Responsive layout (mobile, tablet, desktop) |✅ Done   |
|Firebase sync (bring your own account)      |🔜 Planned|
|iOS Shortcuts share extension               |🔜 Planned|
|Optional AI tagging (bring your own API key)|💡 Idea   |
|Optional PIN lock                           |💡 Idea   |
|Find & resolve existing duplicates          |💡 Idea   |

-----

## 🧠 Philosophy

Most bookmark apps charge a monthly fee, store your data on their servers, and bundle AI you may not want. Stash takes the opposite approach:

- **Local first** — your data lives on your device
- **Free forever** — no subscription, no shared server to maintain
- **Bring your own** — if you want sync, bring your own Firebase; if you want AI, bring your own API key
- **Simple** — one file, no setup, just works

Think of it as a lightweight, private alternative to apps like mymind — for people who want ownership over their data.

-----

## 📄 License

MIT — free to use, modify, and self-host.
