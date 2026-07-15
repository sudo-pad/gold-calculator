# Gold Negotiator

A free, single-file web app for buying, selling, and exchanging gold jewelry with confidence. Pulls live 24K market rates, converts them across karats and units, and instantly shows the making charge / dealer margin baked into any offer — so you know the real numbers before you negotiate.

**Live app:** https://gold.comence.io *(update once your domain is pointed)*

![Gold Negotiator](https://img.shields.io/badge/status-live-brightgreen) ![License](https://img.shields.io/badge/license-MIT-blue)

## Features

- **Live rates** — international spot gold converted to PKR, USD, and CAD via public APIs (no API key required). Manual entry available to match local bazaar rates.
- **Rate board** — tap-to-copy grid of 24K/22K/21K/18K prices per gram, 10g, and tola. "Copy all" formats it for WhatsApp.
- **Buying mode** — enter weight, karat, and asking price; see the implied making charge as an amount and percentage, with a negotiation anchor.
- **Selling mode** — see how far a dealer's offer sits below melt value and the margin they're keeping.
- **Exchange mode** — splits the dealer's take into the trade-in cut and the new-piece premium, and shows what a fair pure-market swap would cost.
- **Quick notes** — jot shop quotes on the go; saved locally on your device.
- **Offline-friendly & persistent** — rates, currency, and notes are cached in the browser between sessions. Add to your home screen to use it like an app.

## Usage

Open the live link, tap **Fetch live** (or enter a rate manually), then pick Buying, Selling, or Exchange. Enter the piece details and read the verdict.

> **Disclaimer:** Estimates only. Rates and verdicts are guides for negotiation, not a professional appraisal or financial advice. Always verify weight, purity, and price with your jeweler.

## Running locally

It's one file — no build step, no dependencies.

```bash
# clone, then just open the file
git clone https://github.com/sudo-pad/gold-calculator.git
cd gold-calculator
open index.html    # or double-click it
```

## Deploying

Hosted free on **GitHub Pages**: Settings → Pages → Deploy from branch → `main` / root. The file must be named `index.html`. To use a custom domain, add it in the Pages settings and create a CNAME record pointing to `sudo-pad.github.io`.

## Tech

Plain HTML, CSS, and vanilla JavaScript. Rate data from [gold-api.com](https://gold-api.com) and [open.er-api.com](https://www.exchangerate-api.com). No frameworks, no tracking, no backend.

## License

MIT — see [LICENSE](LICENSE).

---

Built by [Comence](https://comence.io).
