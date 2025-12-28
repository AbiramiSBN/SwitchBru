# SwitchBru Applications Launcher

A modern, Nintendo Switch–friendly web launcher for **SwitchBru DNS** environments.

This project replaces the old SwitchBru dashboard with a clean launcher UI that supports:
- Games & apps sections
- Controller / D-pad navigation
- Search & URL bar (Google-powered)
- Bookmarks
- JSON-driven app/game lists
- Lightweight, Switch browser–safe HTML/CSS/JS

---

## Features

### 🏠 Home Screen
- **Glowy title UI**: *SwitchBru Applications*
- **Three main tiles**:
  - 🎮 Games
  - 🧩 Apps
  - ⚙️ Settings
- White text optimized for dark backgrounds
- Controller-friendly layout

### 🔍 Search / Omnibox
- Type a **URL** (e.g. `youtube.com`) → opens directly
- Type a **search query** → searches using **Google**
- One-click **Go** button
- Works on Switch browser

### 🔖 Bookmarks
- Built-in bookmark to:
  - **Old SwitchBru Dashboard**  
    `https://dns.switchbru.com/`
- Easily extendable to more bookmarks

### 🎮 Games & Apps Pages
- Loaded dynamically from JSON
- Icons supported (emoji or later images)
- Features:
  - 🔎 Search
  - ⭐ Pin / unpin items
  - ↕ Sort (Pinned first, A→Z, Z→A)
  - 🎮 Controller navigation (D-pad, A/B)
  - ⌨ Keyboard navigation fallback

### ⚙️ Settings
- UI customization options
- Designed for cosmetic preferences
- Uses `localStorage` **best-effort** (non-critical)

---

## Folder Structure

```

/
├─ index.html              # Home launcher
├─ games/
│  └─ index.html           # Games list
├─ apps/
│  └─ index.html           # Apps list
├─ settings/
│  └─ index.html           # Customization UI
├─ JSON/
│  └─ catalog.json         # Games & apps data
├─ assets/
│  ├─ wallpaper.jpeg       # Background
│  └─ (optional icons)

```

---

## JSON Format

All games and apps are defined in:

```

/JSON/catalog.json

````

Example:

```json
{
  "games": [
    {
      "label": "Dino Game",
      "path": "/Dino-Game",
      "icon": "🦖"
    },
    {
      "label": "Seraph Games",
      "path": "https://seraphgames.vercel.app",
      "icon": "🌐"
    }
  ],
  "apps": [
    {
      "label": "Photos",
      "path": "/photos",
      "icon": "📷"
    }
  ]
}
````

* `label` → Display name
* `path` → URL or route
* `icon` → Emoji (safe on Switch)

---

## Controller Controls

### Home

* Navigate tiles using **D-pad / Arrow keys**
* **A / Enter** → Open
* **B / Backspace / Esc** → Go back

### Games / Apps

* D-pad / Arrow keys → Move focus
* **A / Enter** → Launch item
* **⭐ Button** → Pin item
* **B / Esc** → Return to Home

> Gamepad API is used **best-effort**. Keyboard always works.

---

## Browser Compatibility

Optimized for:

* Nintendo Switch browser
* Captive portal / DNS-based browsers
* WebKit-based environments

### Storage Notes

* `localStorage` is used **only for UI preferences & pins**
* Persistence is **not guaranteed** on Switch
* App works even if storage is cleared

---

## Design Goals

* No frameworks
* No heavy JS
* No external dependencies
* Fast load on Switch hardware
* Safe CSS effects only (blur, glow, gradients)

---

## Roadmap / Ideas

* Editable bookmarks via JSON
* Favorites on Home screen
* Image icons per app
* Sound effects (Switch-safe)
* Kiosk / lock mode
* Search across Games + Apps from Home

---

## Credits

Built for the **SwitchBru** community
Designed for Nintendo Switch browser limitations

---

## License

MIT 
