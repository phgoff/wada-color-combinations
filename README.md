# Wada Color Combinations

Interactive browser for the 348 color combinations in Sanzo Wada's *A Dictionary of Color Combinations*.

## What it does

- Shows all 348 palettes as virtualized color stripes.
- Filters by color count, swatch collection, name, and hex.
- Opens a drawer with hex, RGB, and CMYK values.
- Copies CSS variables or JSON for a palette.
- Saves favorites in the browser.

## Run

Open `index.html` in a browser. No build step.

## Agent use

Data is embedded in `index.html` as `<script type="application/json" id="wada-data">` and mirrored in `wada.json`.

JavaScript API on `window.wada`:

- `getPalette(id)`
- `search(query)`
- `exportPalette(id, 'json' | 'css')`
- `favorites()`

DOM hooks: each card has `data-id`; each stripe has `data-hex`.

## Data source

Colors and combinations come from `mattdesl/dictionary-of-colour-combinations` (MIT). Colors are grouped into palettes by inverting the color to combination index.

## License

MIT for code. Palette data follows the upstream MIT license.