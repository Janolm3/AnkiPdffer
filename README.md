# AnkiPdffer

> Export any Anki deck to a polished PDF or a standalone interactive HTML file — in seconds.

---

## Features

- **PDF export** — print-ready output via the built-in Chromium engine, with correct page sizes (A4, Letter, A3, A5) and margins
- **PDF preview** — paginated HTML preview that shows exactly how the PDF will look before printing
- **Legacy HTML** — self-contained single HTML file with embedded images, interactive image lightbox, and optional card grid layout
- **Three themes** — Light ☀️, Dark 🌙, Pro 🔵
- **Full typography control** — 12 font families, adjustable size and line height
- **Card width presets** — Narrow / Medium / Wide / Full / Custom
- **Layout modes** — Standard or Compact
- **Two render sources**:
  - *Fields* — per-field config: assign Front / Back / Extra section, size (S/M/L/XL), bold, label, background color, text color, alignment, italic, underline
  - *Cards (Cloze / Occlusion)* — uses Anki's rendered card templates, SVG occlusion masks preserved
- **Zebra striping**, card numbering, title display
- **Image lightbox** (Legacy HTML) — click any image to open a fullscreen viewer with pinch/scroll zoom, drag to pan, double-click to toggle fit ↔ 100%
- **Grid mode** — display cards in a responsive multi-column grid (toggle in the app before export)
- **Subdeck support** — export a specific subdeck or the whole deck
- **Settings persistence** — save / load / reset all settings to a JSON file
- **English & Polish UI** (language selector in Settings tab — restart required)
- **Debug mode** — export logs to Desktop

---

## Installation

### From AnkiWeb (recommended)
1. Open Anki → **Tools → Add-ons → Get Add-ons**
2. Enter the add-on code: `XXXXXXXX` *(replace with AnkiWeb ID after publishing)*
3. Restart Anki

### Manual install
1. Download the latest `AnkiPdffer.zip` from the [Releases](../../releases) page
2. Open Anki → **Tools → Add-ons → Install from file…**
3. Select the downloaded `.zip`
4. Restart Anki

### Requirements
- Anki **≥ 23.11** (Qt6 recommended; Qt5/PyQt5 fallback supported)
- No external dependencies

---

## Usage

### Open the dialog
**Tools → Export Deck to PDF…**   or press **Shift+P** to instantly export the current deck as Legacy HTML.

### Basic tab
| Setting | Description |
|---|---|
| Theme | Light / Dark / Pro |
| Font | 12 families to choose from |
| Size | Font size in px |
| Width | Card column width (Narrow 520 px … Full) |
| Layout | Standard or Compact spacing |
| Source | Fields (per-field config) or Cards (Cloze/Occlusion) |
| Title / Numbers / Zebra | Toggle deck title, card numbers, alternating row color |

### Advanced tab
| Setting | Description |
|---|---|
| Page | A4 / Letter / A3 / A5 |
| Margins | Page margins in mm |
| Padding | Card inner padding |
| Min gap | Gap between cards |
| Line height | Line spacing multiplier |
| Max img | Maximum image height in px |
| Strip formatting | Remove Anki inline styles |
| Card style | Border/shadow style |

### Fields tab
Configure each note field individually (only active in *Fields* source mode):
- **Section** — assign to Front (top), Back (bottom), or Extra
- **S/M/L/XL** — font size within the card
- **B** — bold
- **Label** — show the field name as a label
- **⋯** — expand for background color, text color, alignment, italic, underline

### Settings tab
- Save / Load / Reset settings to `settings.json` in the add-on folder
- **Language** — English (default) or Polski; restart Anki to apply
- **Debug mode** — show logs button; saves `anki_pdf_log.txt` to Desktop

### Bottom bar
| Control | Description |
|---|---|
| Grid checkbox | Export Legacy HTML with cards arranged in a grid |
| Legacy HTML | Generate a self-contained `.html` file |
| Preview PDF | Paginated preview of the final PDF layout |
| Export PDF | Save as `.pdf` |

---

## Image Viewer (Legacy HTML)

Clicking any image in the exported HTML opens a fullscreen lightbox:

| Action | Result |
|---|---|
| Scroll wheel / trackpad | Zoom in / out (smooth, proportional) |
| Click & drag | Pan the image |
| Double-click | Toggle fit-to-screen ↔ 100% size |
| `Esc` / X button / click background | Close |

---

## Tips

- For **Image Occlusion** cards, switch Source to *Cards (Cloze/Occlusion)* — SVG masks are preserved
- Use **Grid mode** for quick visual review of large decks
- **Shift+P** is a quick shortcut to export the currently focused deck without opening the dialog
- Use **Compact** layout + **No border** card style for the densest output

---

## To Do

- **Better solution for Image Occlusion**
- **Black background in the final PDF**
- **High contrast mode for the quirky styling on the creator of the cards side**

---

## License

MIT — free to use, modify, and distribute.
