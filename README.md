# CAP Capsa Timer

A lightweight, installable countdown timer built as a Progressive Web App (PWA). No frameworks, no dependencies — pure HTML, CSS, and JavaScript.

**Live:** https://inuru.github.io/timer

---

## Features

- Set any countdown duration in seconds
- Visual alert — background turns red when timer reaches zero
- Audio alert — beep sequence in the last 5 seconds (beep, beep, beep, beep, beeeeep)
- One-tap restart from the alarm screen
- Installable on Android and desktop via Chrome
- Works fully offline after first visit

---

## How to Use

1. Enter the number of seconds in the input field
2. Press the **▶** button to start
3. When 5 seconds remain, audio beeps begin
4. At 0, the screen turns red — press **▶** again to restart

---

## Install as App (Android)

1. Open https://inuru.github.io/timer in **Chrome**
2. Tap the 3-dot menu → **Install app** or **Add to Home Screen**
3. The app will appear in your home screen and app drawer

---

## Project Structure

```
├── index.html      # Main app — all UI, logic, and styles in one file
├── manifest.json   # PWA manifest (name, icons, display mode)
├── sw.js           # Service worker for offline caching
├── icon-192.png    # App icon (192x192)
├── icon-512.png    # App icon (512x512)
└── favicon.ico     # Browser tab icon
```

---

## Tech Stack

| Layer | Technology |
|---|---|
| UI | HTML, CSS, Vanilla JavaScript |
| Audio | Web Audio API (oscillator-based beeps, no audio files) |
| Fonts | Google Fonts — Bebas Neue, Share Tech Mono |
| PWA | Web App Manifest + Service Worker |
| Hosting | GitHub Pages |

---

## Local Development

No build step needed. Just open `index.html` directly in a browser for development.

For PWA features (install prompt, service worker, offline), serve over HTTPS or use a local server:

```bash
# Python
python3 -m http.server 8080

# Node
npx serve .
```

Then open `http://localhost:8080`.

---

## License

MIT
