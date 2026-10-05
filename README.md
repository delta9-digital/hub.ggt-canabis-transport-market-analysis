# Going Green Transport (GGT) — Market Analysis Hub

A resource hub for **Going Green Transport**'s cannabis logistics strategy: a structural market
analysis, presentation **decks**, and working **docs**, versioned in one repo and published as a
static site via **GitHub Pages**. _Seed to sale, we never fail._

🔗 **Live hub:** `https://delta9-digital.github.io/hub.ggt-canabis-transport-market-analysis/`

## Brand system

The hub uses the **GGT brand system** (Going Green Transport):

| | |
|---|---|
| Forest green (bg) | `#133f2d` |
| Cream (text / solid fills) | `#efe8d8` |
| Lime (primary accent) | `#bbfd6a` |
| Amber / gold (mono labels) | `#c9a66b` |
| Display font | Bricolage Grotesque (800) |
| Body font | Inter |
| Label / mono font | DM Mono (uppercase, letter-spaced) |

> These tokens were extracted from the GGT `Vehicle Investment: Market Analysis` deck (a Claude
> Design export). The canonical brand source is the Claude Design project
> `claude.ai/design/p/14e648b0-…`; syncing directly to it needs `/design-login` in an interactive
> session. See `assets/styles.css` for the token definitions.

---

## What's here

| Path | Purpose |
|---|---|
| `index.html` | The hub landing page (GitHub Pages entry point). |
| `decks/ggt-vehicle-investment-market-analysis.html` | GGT vehicle-investment deck (18 slides, self-contained, interactive). |
| `docs/market-analysis/` | Starter market analysis — markdown source + a styled viewer page. |
| `docs/` | Working docs. Markdown renders automatically via the viewer pattern. |
| `decks/` | Presentation decks (PDF / PPTX / Keynote exports). |
| `data/` | Supporting data: sizing models, exports, CSVs. |
| `assets/` | Shared stylesheet. |

## How it's published

- GitHub Pages serves this repo from the **`main` branch, root (`/`)**.
- `index.html` is the entry point; `.nojekyll` disables Jekyll so files are served as-is.
- No build step — it's plain HTML/CSS. Markdown docs are rendered **client-side** (the viewer
  fetches the `.md` and renders it), so the markdown file stays the single source of truth.

## Adding content

### A deck
1. Export to PDF (most portable) and drop it in `decks/`.
2. Add a card linking to it in `index.html` under the **Decks** section (copy an existing card).

### A doc
1. Write it as Markdown under `docs/your-doc/your-doc.md`.
2. Copy `docs/market-analysis/index.html` into `docs/your-doc/index.html` and point the `fetch()`
   at your `.md` filename.
3. Add a card to `index.html` under the **Docs** section.

### Data
Drop workbooks / CSVs in `data/` and reference them from the relevant doc.

## Local preview

```bash
# from the repo root
python3 -m http.server 8000
# open http://localhost:8000
```
A static server is needed (not file://) because the doc viewer uses `fetch()`.

---

## ⚠️ Disclaimer

Internal working material. The market analysis is a **structural draft**; all quantitative figures
are **indicative placeholders** (marked `[VALIDATE]`) until sourced. Nothing here is legal, tax, or
investment advice.
