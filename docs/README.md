## 📁 1️⃣ `docs/README.md`

Create a **`docs/` folder** and add this file inside it.

```md
# SwitchBru Launcher – Documentation

This folder contains documentation for the **SwitchBru Launcher**, a custom web launcher designed to run on the Nintendo Switch hidden browser via SwitchBru DNS.

---

## 📌 What is SwitchBru Launcher?

SwitchBru Launcher is a lightweight, controller-friendly web UI that acts like a home menu for the Nintendo Switch browser.

It allows you to:
- Launch games, apps, and websites
- Customize wallpapers and colors
- Use search + bookmarks
- Navigate fully with a controller or keyboard

---

## 🧭 Navigation Overview

### Home
- Central hub with large tiles:
  - Games
  - Apps
  - Web
  - Settings
- Search bar supports:
  - Direct URLs
  - Google search fallback
- Quick bookmarks (hard-coded):
  - Google
  - SwitchBru DNS
  - SwitchBru Games Hub

### Games
- Loads from `JSON/catalog.json`
- Supports:
  - Local games
  - External HTML5 game sites
- Features:
  - Search
  - Sort (A–Z, pinned)
  - Pin favorites
  - Controller navigation

### Apps
- Loads from `JSON/catalog.json`
- Includes AI tools (e.g. PerminiGPT)
- Searchable list
- Simple, fast UI optimized for Switch

### Web
- Curated websites known to work on SwitchBru
- Supports pinning and sorting
- Useful for tools, dashboards, and info pages

### Settings
- UI customization page
- Changes are saved via `localStorage`

---

## 🎨 Customization

### Wallpapers
- Presets:
  - `/assets/wallpaper1.jpeg` → `/assets/wallpaper10.jpeg`
- Legacy support:
  - `/assets/wallpaper.jpeg`
- Custom wallpaper URL:
  - Supports `png`, `jpg`, `jpeg`, `webp`
- Live preview + test button

### Colors
You can customize:
- Global text color
- Title color
- Tile label color
- Button text color

### Layout
- Tile size:
  - Small
  - Normal
  - Large
- Title glow (on/off)
- Custom version string (shown on Home)

---

## 📄 Configuration: `catalog.json`

Location:
```

/JSON/catalog.json

````

Structure:
```json
{
  "games": [],
  "apps": [],
  "web": []
}
````

Each entry:

```json
{
  "label": "Display Name",
  "path": "https://example.com",
  "icon": "🎮"
}
```

### Notes

* Emoji icons are recommended (safe on Switch)
* SVGs and heavy images may not load
* External sites should be tested on Switch

---

## 🎮 Controls

| Action   | Input               |
| -------- | ------------------- |
| Navigate | D-pad / Arrow keys  |
| Select   | A / Enter           |
| Back     | B / Backspace / Esc |
| Pin      | ⭐ button            |
| Search   | On-screen keyboard  |

Gamepad support uses `navigator.getGamepads()` and is best-effort.

---

## ⚠️ Switch Browser Limitations

* WebKit-based captive portal browser
* No extensions
* Limited memory
* `localStorage` may clear
* Some JS-heavy sites may fail

Design choices prioritize:

* Simplicity
* Low JS overhead
* Emoji-based icons

---

## 🧪 Testing Tips

* Test on real hardware whenever possible
* Avoid autoplay video backgrounds
* Prefer static assets
* Keep layouts simple and large

---

## 📚 Related Files

* `/index.html` – Home
* `/games/index.html` – Games
* `/apps/index.html` – Apps
* `/web/index.html` – Web
* `/settings/index.html` – Settings
* `/JSON/catalog.json` – Data source

---

## 🛠️ Extending the Launcher

Ideas:

* Auto-load homepage bookmarks from JSON
* Add badges (tested / unstable)
* Export/import settings
* Offline fallback pages

---

Nintendo Switch is a trademark of Nintendo.
This project is unofficial and for educational / personal use.
