# 📦 Stash

> Your personal archive. Stored on your device, free forever.

Stash is a lightweight, privacy-first bookmarking and note-saving app that runs entirely in your browser. No account. No server. No subscription. Your data never leaves your device.

-----

## ✨ Features

- **Save anything** — web pages, notes, ideas, links
- **Stash Clip** — one-tap saving from any page in any browser via a bookmarklet
- **Tap to open** — tap any card to open the URL or edit a note
- **Tags inline** — tags shown on same row as title, tap to filter instantly
- **Swipe to delete** — swipe left on any card
- **Swipe to edit** — swipe right on any card to edit title, tags, description
- **Tag suggestions** — existing tags shown as tappable pills when editing
- **Smart URL display** — search engine URLs hidden from cards but still tappable
- **Date groups** — items grouped by Today, Yesterday, This Week, This Month
- **Search & filter** — search titles, descriptions, URLs and tags
- **Sort** — newest, oldest, A–Z, Z–A
- **Duplicate detection** — merge, replace, keep both or cancel
- **Import / Export** — your data as JSON, fully portable
- **Daily backup** — prompted every 24hrs to save a backup file to your device
- **Shadow backup** — automatic localStorage copy, auto-restores if data is lost
- **Works offline** — service worker caches the app for offline use
- **Installable on iPhone** — add to home screen via Safari
- **Responsive** — works on phone, tablet and desktop

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

> ⚠️ **Important:** Use Stash in Safari (not the home screen icon) if you want Stash Clip to work. iOS stores data separately for each context.

-----

## 🤖 Install on Android

1. Open your Stash URL in **Chrome**
1. Tap the **three dot menu** (⋮) at the top right
1. Tap **“Add to Home Screen”**
1. Tap **Add**

Stash installs as a PWA and opens fullscreen just like a native app.

**Web Clip on Android:**
The bookmarklet works in Chrome on Android too. Follow the same Stash Clip setup steps but in Chrome — add a bookmark, edit it, paste the code.

-----

## 💻 Use on Desktop

Just open your Stash URL in any browser — Chrome, Firefox, Safari, Edge. No install needed.

To save pages quickly on desktop, the bookmarklet works in every browser:

1. Go to the **🔖 Stash Clip** tab inside Stash
1. Copy the code
1. Create a new bookmark in your browser
1. Replace the URL with the copied code
1. Name it **“Stash It”** and save it to your bookmarks bar

Now one click saves any page to Stash from your desktop browser.

-----

## 🌐 Browser Support

|Browser          |Use Stash|Install as App|Web Clip|
|-----------------|---------|--------------|--------|
|Safari (iPhone)  |✅        |✅ Best        |✅       |
|Chrome (Android) |✅        |✅             |✅       |
|Chrome (desktop) |✅        |✅             |✅       |
|Firefox (desktop)|✅        |✅             |✅       |
|Safari (Mac)     |✅        |✅             |✅       |
|Edge (desktop)   |✅        |✅             |✅       |
|Chrome (iPhone)  |✅        |⚠️ Limited     |✅       |


> ⚠️ Chrome on iPhone can open Stash fine but Apple restricts PWA installs to Safari only on iOS.

-----

## 🔖 Stash Clip Setup

Stash Clip lets you save any page to Stash with one tap — works in Safari, Chrome, Firefox and any browser.

1. Go to the **🔖 Stash Clip** tab inside Stash
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

## 🚀 Using Stash

**Option 1 — Use the hosted version (easiest)**
Just open this URL in Safari on your iPhone — no setup needed:

```
https://ritesh009.github.io/Stash/
```

Add it to your home screen and you’re done. Free, no account required.

**Option 2 — Host it yourself on GitHub Pages (also free)**
If you want your own copy at your own URL:

1. [Fork this repo](https://github.com/ritesh009/Stash/fork) on GitHub
1. Go to your forked repo → **Settings → Pages**
1. Under **Source**, select **Deploy from a branch → main → / (root)**
1. Click **Save**
1. Your Stash will be live at `https://YOUR-USERNAME.github.io/Stash/`

That’s it — completely free, no domain purchase needed, no server to maintain.

> Both options are free. The only difference is Option 2 gives you your own private URL and full control over the code.

-----

## 🗺 Roadmap

|Feature                                                    |Status   |
|-----------------------------------------------------------|---------|
|Save notes & web pages                                     |✅ Done   |
|Tags, search, sort, filter                                 |✅ Done   |
|Stash Clip bookmarklet                                     |✅ Done   |
|Swipe to edit / delete                                     |✅ Done   |
|Tag suggestions in edit sheet                              |✅ Done   |
|Inline tags on cards                                       |✅ Done   |
|Tap card to open URL or edit                               |✅ Done   |
|Import / Export                                            |✅ Done   |
|Duplicate detection                                        |✅ Done   |
|Daily backup prompts                                       |✅ Done   |
|Privacy — no Google fonts or favicons                      |✅ Done   |
|Responsive layout (mobile, tablet, desktop)                |✅ Done   |
|Multi-format import (browser bookmarks, Raindrop, Obsidian)|🔜 Planned|
|Optional AI tagging (bring your own API key)               |💡 Idea   |
|Optional PIN lock                                          |💡 Idea   |
|Find & resolve existing duplicates                         |💡 Idea   |
|App icon                                                   |💡 Idea   |

-----

## 🔄 Why no cloud sync?

Stash is intentionally local-first. We explored adding Firebase sync but decided against it — Firebase is a Google product, which contradicts Stash’s privacy-first philosophy.

The iOS platform also makes true private sync without a server technically impossible — Apple sandboxes the home screen PWA and Safari as completely separate storage contexts with no way to bridge them without a third-party server.

**The recommended approach:**
Use Stash in **Safari** (not the home screen icon) for the best experience. Stash Clip works there, data persists reliably, and the daily backup prompt keeps you safe.

To move data between devices manually, use **Share → Export** on one device and **Share → Import** on the other.

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