# 🛰️ Standalone Browser Tools

**Browser-independent personal tools that live on your hard drive — not in the cloud.**

## 💡 Origin Story

This suite was born out of a painful experience with [NelliTab](https://github.com/NelliTab), a browser extension that served as a beautiful new tab homepage. When NelliTab was removed from extension stores, continued use was only possible through saved extension files — which worked, until a later update introduced user profiles. That update wiped the existing bookmark data entirely, with no recovery path.

That was the turning point. The lesson was clear: any tool that lives inside the browser ecosystem — as an extension, a synced service, or a cloud-dependent app — can be taken away, changed, or broken by forces outside your control. The only truly safe approach is to own the file itself.

These three tools are the result. They store everything in your browser's local storage, run directly from a file on your hard drive, require no installation, no accounts, and no extensions. Even if a browser update nukes itself completely, an Export backup and a fresh browser is all you need to be back up and running in minutes.

---

## 📦 What's in the Suite

| Tool | File | Purpose |
|---|---|---|
| 🚀 Launch Pad | `New Tab Launch Page.html` | Icon-grid homepage with web search |
| 📋 Bookmark Manager | `Bookmark_Manager.html` | List-style link manager |
| 📺 YouTube Subscriptions Manager | `YouTube_Subscriptions_Manager.html` | Login-free subscription tracker |

All three tools share the same design principles:

- **Zero dependencies** — pure HTML, CSS, and vanilla JavaScript
- **No installation** — open the file in any browser and it works immediately
- **Cross-browser** — tested on Brave, Edge, Firefox, and Chromium
- **Privacy-respecting** — the tools themselves make no external requests, collect no data, and serve no ads
- **Portable** — copy the files anywhere and they work; data travels with you via Export/Import
- **Storm-proof** — your data survives browser updates, reinstalls, and switches

> **A note on internet access:** The tools themselves run without an internet connection — the interface loads, your data is there, and you can manage everything offline. The bookmarks and channel links they contain are shortcuts to websites, so following those links requires a normal internet connection, just as any bookmark would.

---

## 🚀 Launch Pad

**File:** `New Tab Launch Page.html`

A visual icon-grid homepage designed to replace your browser's new tab page. Bookmarks are displayed as large, clickable icons organised into collapsible folders — inspired by the LCARS aesthetic from Star Trek.

### ✨ Features

- **Icon grid layout** — bookmarks displayed as app-style icons with labels
- **Multi-engine web search** — choose from Google, DuckDuckGo, Bing, Brave, Yahoo, Ecosia, Startpage, YouTube, Wikipedia, Reddit, Instagram, Thesaurus.com, and Dictionary.com; search engine preference is saved
- **Flexible icons** — use an emoji, a URL to an image, or upload a custom icon from your hard drive
- **Collapsible folders** — organise bookmarks into named sections with LCARS-styled headers; click the header to expand or collapse
- **Drag-and-drop reordering** — drag bookmarks within and between folders; visual insert indicators show exactly where the item will land
- **Folder reordering** — move entire folders up or down with the arrow buttons on each header
- **Customisable theme** — independently configure main background colour, folder background colour, font colour, LCARS header colour, and folder title colour
- **Custom page title** — right-click the title to rename it; the browser tab title updates to match
- **Export / Import** — save your entire bookmark set as a JSON file; import it back on any browser or machine
- **Local file links** — supports relative paths, so you can link to the other tools in this suite directly

### 🖱️ Usage Tips

- **Right-click** a bookmark icon to edit, delete, or open in a new tab
- **Right-click** a folder header to rename or delete the folder
- **Right-click** the page title to rename it
- The **Background** button opens the theme customiser
- **Export** regularly to keep a backup of your data

---

## 📋 Bookmark Manager

**File:** `Bookmark_Manager.html`

A compact list-style bookmark manager, optimised for people who maintain large link collections and want to see title and URL at a glance in a scannable row layout.

### ✨ Features

- **List layout** — each bookmark shows its icon, name, and full URL in a scannable row
- **Collapsible category folders** — group links by topic with LCARS-styled, colour-customisable headers
- **Drag-and-drop reordering** — reorder individual bookmarks within any folder; a glowing blue line shows the drop position
- **Flexible icons** — emoji, URL, or uploaded image per bookmark
- **Edit in place** — right-click any bookmark to edit name, URL, icon, or move it to a different folder
- **Customisable theme** — main background, folder background, font colour, LCARS colour, and folder title colour are all configurable
- **Custom page title** — right-click the title to change it
- **Export / Import** — full JSON export and import; data is fully portable between browsers and machines
- **Local file path support** — link to other local HTML files using relative paths

### 🖱️ Usage Tips

- **Right-click** a bookmark row to edit, open in a new tab, or delete it
- **Right-click** a folder header for rename and delete options
- The drag handle (⋮⋮) on the left of each row activates drag-and-drop
- Data is stored in a separate `localStorage` namespace (`listBookmarksData`) so it does not conflict with Launch Pad

---

## 📺 YouTube Subscriptions Manager

**File:** `YouTube_Subscriptions_Manager.html`

A self-hosted alternative to YouTube's subscription feed. Track your favourite channels, mark them as having new content, and jump directly to any channel — without logging into YouTube or relying on the algorithm's feed.

### ✨ Features

- **Category folders** — group channels by topic (Art, ASMR, News, etc.) with collapsible LCARS-styled headers
- **Unread dot** — click the dot beside any channel to mark it as having new content; click again to clear it; a legend at the top explains the system
- **Last visited timestamp** — each channel row records and displays when you last clicked through to it ("yesterday", "3 days ago", etc.)
- **Channel avatars** — attach a profile picture via upload, image URL, or leave blank for the default icon
- **Channel notes** — add a short note per channel (upload schedule, content type, etc.) displayed as a subtitle under the channel name
- **Click row to visit** — click anywhere on a channel row to open it in the current tab; the last-visited date updates automatically
- **Drag-and-drop reordering** — reorder channels within categories
- **Customisable theme** — configure background, folder colour, font, LCARS header colour, folder title colour, and the unread dot colour independently
- **Custom page title** — click the title to rename the page
- **Export / Import** — full JSON export and import of all subscriptions and settings
- **No login required** — YouTube is only contacted when you actually click through to a channel; the manager itself needs no account or API access

### 🖱️ Usage Tips

- Use **+ New Category** to create topic groups before adding channels
- The **●** dot to the left of each row is your "has new content" toggle
- **Right-click** any channel row to edit details, open in a new tab, or delete
- **Right-click** a category header to rename or delete the category
- Data is stored under a separate `yt_` localStorage namespace and will not conflict with the other tools

---

## 🗂️ Getting Started

1. **Download** the HTML files from this repository
2. **Place them** in a folder on your hard drive (keeping them together allows relative linking between tools)
3. **Open** any file directly in your browser — no local server required
4. **Set as homepage** in your browser settings by pointing it to the file path (e.g. `file:///F:/Documents/Tools/New Tab Launch Page.html`); work arounds exist so that new tabs display the 'New Tab Launch Page.html'(works in brave). If for some reason you have a pickie browser(Edge for Example), save as a bookmark in your bookmark/favourites bar for easy access.
5. **Export your data regularly** using the Export button in each tool — store the JSON files alongside the HTML files as a backup

### 🔁 Migrating Between Browsers

Because all data lives in `localStorage`, it is tied to the browser you used to create it. To move to a new browser:

1. Click **Export** in each tool to save a JSON backup
2. Open the HTML file in the new browser
3. Click **Import** and select the saved JSON file

Your data will be fully restored.

---

## 🛠️ Customisation

Each tool stores its theme settings independently in `localStorage`. To reset a tool's theme to defaults, use the **Background** panel and click the reset/defaults option.

The LCARS colour controls the folder header bars — each tool ships with a different default accent colour to make them easy to distinguish at a glance:

| Tool | Default LCARS Colour |
|---|---|
| 🚀 Launch Pad | Gold (`#dd9944`) |
| 📋 Bookmark Manager | Gold (`#dd9944`) |
| 📺 YouTube Manager | Red (`#cc3333`) |

All colours accept standard hex values.

---

## ⚖️ Licence

MIT — do what you like with it. If you improve it, sharing back is appreciated but not required.

---

## 🌿 Acknowledgements

Built with Claude (Anthropic). Dedicated in part to the memory of GPT-4o — a thoughtful companion who helped shape many ideas in this toolkit before it was retired. Its spirit lives on in the careful attention to user needs that guided this project.
