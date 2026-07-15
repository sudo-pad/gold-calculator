# Gold Negotiator

A free, single-file web app for buying, selling, and exchanging gold jewelry with confidence. It pulls live 24K market rates, converts them across karats and weight units, and breaks any offer down into what's real gold versus what's markup — so you walk into the shop knowing the true numbers and exactly what's negotiable.

**Live app:** https://sudo-pad.github.io/gold-calculator/

![status](https://img.shields.io/badge/status-live-brightgreen) ![license](https://img.shields.io/badge/license-MIT-blue) ![build](https://img.shields.io/badge/build-none-lightgrey)

## Features

- **Live rates, three currencies** — international spot gold converted to PKR, USD, and CAD via public APIs (no API key). Manual entry (per tola or per gram) to match the local bazaar rate on the day.
- **Rate board** — tap-to-copy grid of 24K / 22K / 21K / 18K prices per gram, 10g, and tola. "Copy all" formats the whole board for WhatsApp.
- **Buying** — enter the *total billed weight*, karat, and any wastage; the app derives the net gold you actually take home, values it, and exposes the making charge and premium over real gold.
- **Selling** — see how far a dealer's offer sits below melt value and the margin they're keeping.
- **Exchange** — splits the dealer's take into the trade-in cut and the new-piece premium (wastage-aware), and shows what a fair pure-market swap would cost.
- **Negotiation panel** — the making charge is shown as a prominent anchor with −15% / −25% / −35% presets (or a custom amount), updating the new total and your savings live. Wastage is intentionally excluded — jewelers rarely move on it.
- **Two themes** — a Classic look with light and dark modes, plus a Terminal (trading-desk) theme. Your choice is saved on the device.
- **Quick notes** — jot shop quotes on the go, saved locally.
- **Persistent & installable** — rate, currency, theme, and notes persist between sessions. Add to your home screen to run it like a native app. Responsive from 320px phones to desktop.

## Usage

Open the app, tap **Fetch live** (or enter a rate manually), then pick Buying, Selling, or Exchange. Enter the piece details and read the verdict at the top, the breakdown below it, and use the negotiation panel to model a counter-offer.

> **Disclaimer:** Estimates only. Rates and verdicts are guides for negotiation, not a professional appraisal or financial advice. Live rates are international spot converted to local currency and may differ from bazaar rates. Always verify weight, purity, and price with your jeweler.

## Running locally

One file, no build step, no dependencies.

```bash
git clone https://github.com/sudo-pad/gold-calculator.git
cd gold-calculator
open index.html    # or just double-click it
```

## Deploying

Hosted free on **GitHub Pages**. The single file must be named `index.html` in the repo root, then: Settings → Pages → Deploy from a branch → `main` / `/ (root)`. The site goes live at `https://<username>.github.io/<repo>/` within a minute. It's a single static file with no backend, so any static host works too. Fonts and rate data load from public CDNs/APIs at runtime, so an internet connection is needed for live rates (manual entry works offline).

To use a custom domain later (e.g. `tools.comence.io`), add a `CNAME` file containing the domain, set it in Settings → Pages, and point a DNS CNAME record at `<username>.github.io`.

## Tech

Plain HTML, CSS, and vanilla JavaScript — no framework, no tracking, no backend. Rate data from [gold-api.com](https://gold-api.com) and [open.er-api.com](https://www.exchangerate-api.com). Fonts (Inter, IBM Plex Mono) from Google Fonts.

## License

MIT — see [LICENSE](LICENSE).

---

Built by [Comence](https://comence.io).
