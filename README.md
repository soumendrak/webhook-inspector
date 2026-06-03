<p align="center">
  <svg width="120" height="120" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
    <rect width="100" height="100" rx="20" fill="#1a1a2e"/>
    <path d="M25 35 C25 25, 45 20, 50 30 C55 20, 75 25, 75 35" stroke="#ff6b35" stroke-width="5" stroke-linecap="round" fill="none"/>
    <path d="M30 45 C30 38, 45 35, 50 42 C55 35, 70 38, 70 45" stroke="#ff6b35" stroke-width="4" stroke-linecap="round" fill="none"/>
    <circle cx="50" cy="60" r="14" stroke="#ff6b35" stroke-width="4" fill="none"/>
    <circle cx="50" cy="60" r="5" fill="#ff6b35"/>
    <path d="M50 74 L50 82" stroke="#ff6b35" stroke-width="3" stroke-linecap="round"/>
    <path d="M40 80 L60 80" stroke="#ff6b35" stroke-width="2" stroke-linecap="round"/>
  </svg>
</p>

# Webhook Inspector

> **A client-side webhook viewer and inspector — no server required.**  
> Paste, parse, filter, and inspect webhook payloads right in your browser.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-live-success?logo=github)](https://soumendrak.github.io/webhook-inspector/)
[![Zero Dependencies](https://img.shields.io/badge/dependencies-0-brightgreen)](#)
[![Made with](https://img.shields.io/badge/made%20with-vanilla%20JS-orange)](#)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen)](#)

---

## ✨ Features

- 📥 **Paste JSON payloads** — auto-validates and pretty-prints any JSON you paste
- 📋 **Header editor** — add/edit/remove HTTP headers to simulate real webhook delivery
- 🔍 **Search & filter** — full-text search across payloads, headers, and paths
- 💾 **Persistent history** — all webhooks saved in `localStorage`, survives page reloads
- 🎨 **Dark theme** — eye-friendly dark UI with orange accent, fully customizable via CSS vars
- 📱 **Responsive** — works beautifully on desktop, tablet, and mobile
- ⚡ **Zero dependencies** — no frameworks, no build tools, no npm. Just a single HTML file.
- 🚀 **GitHub Pages ready** — deploy by pushing to any repo with Pages enabled

## 🚀 Quick Start

### Option 1: Use GitHub Pages (live)

Visit **[https://soumendrak.github.io/webhook-inspector/](https://soumendrak.github.io/webhook-inspector/)**

### Option 2: Open locally

```bash
git clone https://github.com/soumendrak/webhook-inspector.git
cd webhook-inspector
open index.html   # or double-click in your file manager
```

That's it. No server, no install, no build step.

## 🖥️ Usage

1. **Paste a JSON payload** in the left panel — the app validates it in real time
2. **Add or edit headers** to simulate what a real webhook provider would send
3. **Click "Simulate Webhook"** — the payload appears in the history panel on the right
4. **Click any history entry** to inspect headers and body in a detail view
5. **Search history** using the search box to find specific payloads
6. **Clear history** with the "Clear" button in the header bar

### Preset examples

Click any preset button to load a sample payload:

| Preset | Description |
|--------|-------------|
| **GitHub push** | Simulates a GitHub push event webhook |
| **Stripe event** | Simulates a `charge.succeeded` Stripe webhook |
| **Slack message** | Simulates a Slack message event |
| **Custom** | A minimal empty template to start from |

## 🎨 Customization

The app uses CSS custom properties for theming. Override them in your browser's dev tools or fork and edit:

```css
:root {
  --bg: #0f0f1a;      /* page background */
  --surface: #1a1a2e;  /* card/surface background */
  --accent: #ff6b35;   /* accent color */
  --text: #e0e0e0;     /* text color */
  --border: #2a2a3e;   /* border color */
}
```

To add more preset payloads, edit the `presets` section in `index.html` — add a new `<button data-preset="mypreset">` and a matching `case` in the JavaScript.

## 📸 Screenshot

<p align="center">
  <img src="https://raw.githubusercontent.com/soumendrak/webhook-inspector/main/screenshot.png" alt="Webhook Inspector screenshot" width="720">
  <br>
  <em>Replace the screenshot link above with an actual screenshot of the app in action.</em>
</p>

## 🧱 Architecture

```
webhook-inspector/
├── index.html    # Single-file app (HTML + CSS + JS)
├── LICENSE       # MIT License
└── README.md     # This file
```

Everything is in one file. The app uses:
- **localStorage** for persistent webhook history
- **CSS Grid/Flexbox** for responsive layout
- **CSS custom properties** for theming
- **No external dependencies** whatsoever

## 🤝 Contributing

PRs are welcome! If you'd like to add features, fix bugs, or improve the docs:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing`)
3. Commit your changes (`git commit -am 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing`)
5. Open a Pull Request

## 📄 License

This project is [MIT](LICENSE) licensed. Use it freely in personal and commercial projects.

---

<p align="center">
  Built with ❤️ and vanilla JavaScript.
</p>
