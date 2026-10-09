# Prank Website

A playful, multi-step prank page disguised as a normal “Get Started” flow. Visitors think they’re setting something up — instead they get a harmless chain of fake loading screens, evasive buttons, absurd terms of service, and multiplying pop-ups before the big reveal.

No build step, no backend, no dependencies to install. Open the HTML file or serve it locally and share the link with someone who’s in on the joke.

## What happens

The prank runs as a linear sequence of scenes:

1. **Fake loading screen** — A progress bar fills to 100%, then reverses with increasingly suspicious status messages (“Calibrating flux capacitor…”, “Unloading.”) before finally moving on.
2. **Runaway button** — A “Press Start to Continue” button teleports around the screen on hover or click, taunting the user with messages like “Almost…” and “Nope.” After enough attempts, it gives up.
3. **Fake Terms of Service** — A modal with deliberately ridiculous legal gibberish. The accept button stays disabled until the user scrolls to the bottom.
4. **Hydra pop-ups** — Closing a pop-up spawns ten more (fake V-Bucks, “download more RAM”, cookie consent, etc.). After closing ten pop-ups total, the chaos stops.
5. **Grand finale** — A “You’ve Been Pranked!” screen with confetti and a restart button to run the whole thing again.

## Tech stack

- Plain HTML, CSS, and vanilla JavaScript — no bundler or framework
- [Tailwind CSS](https://tailwindcss.com/) via CDN for layout and styling
- [canvas-confetti](https://www.npmjs.com/package/canvas-confetti) via CDN for the finale celebration
- [Inter](https://fonts.google.com/specimen/Inter) from Google Fonts

## Project structure

| File | Purpose |
|------|---------|
| `index.html` | Page markup and prank “screens” (loading, runaway button, ToS modal, finale) |
| `style.css` | Custom animations and overrides (runaway button transition, pop-up pop-in) |
| `script.js` | Prank logic: loading bar, button positioning, ToS scroll gate, pop-up spawning |

## How to run

**Option 1 — Open directly**

Double-click `index.html` or drag it into your browser.

**Option 2 — Local server (recommended)**

Some browsers behave more predictably when the page is served over HTTP:

```bash
# Python 3
python3 -m http.server 8000

# Node (if npx is available)
npx serve .
```

Then visit `http://localhost:8000` (or the port shown in your terminal).

## Notes & safety

- Keep it friendly and consensual. This is meant for people who will laugh, not for tricking strangers or causing real frustration.
- Don’t use it to collect data, impersonate real services, or deploy anything that could be mistaken for malware or phishing.
- If you share or host the page, make sure participants know it’s a joke.

## License

MIT License. See `LICENSE` if present.

## Contact

Repository owner: [JacintoDesign](https://github.com/JacintoDesign)
