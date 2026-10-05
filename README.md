# GGT Cannabis Transport — Market Analysis Hub

A resource hub for the **cannabis transport** market: a structural market analysis plus a home for
presentation **decks** and working **docs**, versioned in one repo and published as a static site via
**GitHub Pages**.

🔗 **Live hub:** `https://delta9-digital.github.io/hub.ggt-canabis-transport-market-analysis/`
_(available once GitHub Pages finishes its first build)_

---

## What's here

| Path | Purpose |
|---|---|
| `index.html` | The hub landing page (GitHub Pages entry point). |
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
