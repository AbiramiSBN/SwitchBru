# SwitchBru Launcher

A custom web-based launcher designed for the Nintendo Switch hidden browser using **SwitchBru DNS**.  
This project provides a clean, controller-friendly home screen with **Games, Apps, Web**, and **Settings**, plus search, bookmarks, and customization.

---

## ✨ Features

### 🏠 Home
- Large, rounded tiles (Games / Apps / Web / Settings)
- URL + Google search bar
- Hard-coded quick bookmarks:
  - Google
  - SwitchBru DNS (legacy dashboard)
  - SwitchBru Games Hub
- Glowy title bloom
- Fully controller-friendly

### 🎮 Games
- Loads dynamically from `catalog.json`
- Supports:
  - Local games (e.g. Dino Game)
  - External game portals (ArmorGames, Kongregate, Poki, etc.)
- Search, sort, pin
- D-pad / keyboard navigation

### 🧩 Apps
- Loads dynamically from `catalog.json`
- Includes AI apps like **PerminiGPT**
- Search + quick launch
- Switch-safe layout

### 🌐 Web
- Curated list of websites known to work on SwitchBru
- Examples:
  - Google
  - Wikipedia
  - SwitchBru DNS
  - FBI Bears
  - Moldeo tools
- Pin, search, sort
- Controller navigation

### ⚙️ Settings
- Wallpaper presets (`wallpaper1.jpeg` → `wallpaper10.jpeg`)
- Custom wallpaper URL (png / jpg / jpeg / webp)
- Live preview + test
- Text color customization:
  - Global text
  - Title
  - Tile labels
  - Buttons
- Tile size (small / normal / large)
- Title glow toggle
- Version text
- Saved via `localStorage` (best-effort on Switch)

---

## 📁 Project Structure

```

/
├─ index.html                # Home screen
├─ games/
│  └─ index.html             # Games page
├─ apps/
│  └─ index.html             # Apps page
├─ web/
│  └─ index.html             # Web bookmarks page
├─ settings/
│  └─ index.html             # Settings UI
├─ JSON/
│  └─ catalog.json           # Games / Apps / Web config
├─ assets/
│  ├─ wallpaper.jpeg
│  ├─ wallpaper1.jpeg
│  ├─ wallpaper2.jpeg
│  └─ ...
└─ README.md

````

---

## 📄 `catalog.json` Format

```json
{
  "games": [
    { "label": "Dino Game", "path": "/games/DinoGame/", "icon": "🦖" }
  ],
  "apps": [
    { "label": "PerminiGPT", "path": "https://perminigpt.vercel.app/", "icon": "🤖" }
  ],
  "web": [
    { "label": "Google", "path": "https://www.google.com", "icon": "🔎" }
  ]
}
````

* **label** → Display name
* **path** → URL or local path
* **icon** → Emoji (safe for Switch browser)

---

## 🎮 Controls

| Action | Input               |
| ------ | ------------------- |
| Move   | D-pad / Arrow keys  |
| Select | A / Enter           |
| Back   | B / Backspace / Esc |
| Pin    | ⭐ button            |
| Search | On-screen keyboard  |

(Gamepad support is best-effort via `navigator.getGamepads()`.)

---

## 🧠 Notes About the Switch Browser

* Uses Nintendo’s hidden WebKit browser
* No extensions
* `localStorage` may clear unexpectedly
* Emoji icons are safest (no SVGs)
* Heavy JS/video sites may not work

---

## 🚀 Usage

1. Set your Switch DNS to **SwitchBru**
2. Open the internet test page
3. Load your hosted launcher
4. Bookmark it
5. Enjoy a console-style web launcher 🎉

---

## 🔮 Planned Ideas

* Auto-pin favorite apps
* Theme presets (OLED / Neon / Dark)
* Animated wallpapers with fallback
* Export / import settings
* Offline cached pages

---

## 📜 License

This project is experimental and for educational / personal use only.
Nintendo Switch is a trademark of Nintendo.
- Generate a **docs/** folder with usage guides
```
