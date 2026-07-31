# Assassin's Creed — The Journey Saga

A single-page, data-driven fan site covering all 14 mainline *Assassin's Creed* games — from **Assassin's Creed (2007)** to **Assassin's Creed Shadows (2024)**. Browse every protagonist, story, supporting cast, and assassination target in one interactive experience.

> ⚠️ **Fan Project Disclaimer** — This is an unofficial, non-commercial fan site. *Assassin's Creed*, Ubisoft, and all related logos, characters, and assets are trademarks of **Ubisoft Entertainment**. This project is not affiliated with or endorsed by Ubisoft.

---

## ✨ Features

- **Full Saga Grid** — All 14 games with cover art, release year, setting, era, and protagonist at a glance
- **Detailed Modals** — Click any game for its full story, protagonist stats (born, died, affiliation, rank, weapons, voice actor), supporting cast, modern-day framing narrative, and key assassination targets
- **Live Search** — Filter games instantly by title, protagonist, setting, or era
- **Interactive Timeline** — All games sorted chronologically by *in-universe* year (handles BCE eras correctly)
- **Keyboard Navigation** — `←` / `→` to move between games in the modal, `Esc` to close
- **Smooth Animations** — Scroll-reveal effects, floating particles, parallax hero crest, and animated transitions
- **Fully Responsive** — Collapsible hamburger nav and adaptive grid for mobile/tablet
- **Zero Dependencies** — Pure HTML, CSS, and vanilla JavaScript — no frameworks, no build step

## 🖥️ Preview

| Hero | Games Grid | Game Detail Modal |
|---|---|---|
| Landing page with animated crest | Searchable card grid | Full story, cast & targets |

## 🚀 Getting Started

No build tools or dependencies required.

```bash
git clone https://github.com/Skyborg141/Assasins-Creed-Website.git
cd Assasins-Creed-Website
```

Then simply open the HTML file in your browser:

```bash
open Assassins_Creed_Journey_Saga_Wallpapers.html   # macOS
start Assassins_Creed_Journey_Saga_Wallpapers.html  # Windows
```

Or serve it locally for a proper environment:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## 🧱 Tech Stack

- **HTML5** — semantic structure
- **CSS3** — custom properties, clip-path, backdrop-filter, CSS Grid/Flexbox
- **Vanilla JavaScript** — DOM rendering, `IntersectionObserver` for scroll reveals, no libraries
- **Google Fonts** — [Cinzel](https://fonts.google.com/specimen/Cinzel) & [Crimson Text](https://fonts.google.com/specimen/Crimson+Text)

## 📁 Project Structure

```
Assasins-Creed-Website/
├── Assassins_Creed_Journey_Saga_Wallpapers.html   # Single-file site (HTML + CSS + JS)
├── aclogo.png                                     # Site crest / logo
└── README.md
```

All content is driven by a single `games` array in the embedded `<script>` — each entry holds the game's metadata, protagonist details, cast, full story text, modern-day framing, and key targets. Adding a new game means adding one object to that array; the grid, timeline, search index, and modal all render from it automatically.

## 🛠️ Customization

To add or edit a game, find the `games` array and add an object following the existing schema:

```js
{
  id: "ac-example",
  image: "https://...",
  title: "Assassin's Creed: Example",
  year: 2025,
  order: 1500,          // in-universe year, used for timeline sorting (negative = BCE)
  setting: "...",
  era: "...",
  color: "#hexcolor",
  protagonist: { name, born, died, affiliation, rank, weapons, voice },
  cast: [ { name, role, desc }, ... ],
  storyShort: "...",
  storyFull: "...",
  modernDay: "...",
  keyTargets: [ "...", "..." ]
}
```

## 📄 License

The code in this repository is free to use and modify for personal/non-commercial purposes. All *Assassin's Creed* names, characters, artwork, and related IP remain the property of **Ubisoft Entertainment**.

## 🙌 Credits

Built by [Shouvik Banerjee](https://github.com/Skyborg141) as a fan tribute to the *Assassin's Creed* series.
