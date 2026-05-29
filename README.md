[English](./README.md) | [Português (Brasil)](./README.pt-BR.md)

# PDF Dark Mode

Dark-mode PDF reader that runs entirely in the browser, with highlights, text comments, search, zoom, print copy, and annotated PDF export.

## Overview

PDF Dark Mode is a lightweight client-side reader built for comfortable long-form reading. It lets you open a PDF locally, switch between dark presets, navigate quickly, highlight content, add styled comments, and export the annotated file without a backend.

## Features

- Dark reading presets: `Warm`, `Classic`, and `Blue`
- Search with visible current-match emphasis
- Stable page navigation, thumbnails, and page jump
- Text highlight and box highlight tools
- Click-to-place text comments with size, bold, and italic styles
- Undo and redo with `Ctrl + Z` / `Ctrl + Y`
- Copy the current page as an image
- Export annotated PDF locally
- Custom annotation color persisted in `localStorage`

## Tech Stack

- HTML
- CSS
- Vanilla JavaScript
- [PDF.js](https://mozilla.github.io/pdf.js/)
- [PDF-lib](https://pdf-lib.js.org/)

## Run Locally

### Option 1: open directly

Open `index.html` directly in the browser.

Notes:
- some browser APIs may be limited under `file://`
- `Save as` works best when served from `localhost`

### Option 2: recommended local server

```bash
python -m http.server 5500
```

Then open:

```text
http://localhost:5500
```

## Usage

### Highlight text

1. Click `Caneta`
2. Select text inside the PDF

### Draw a box highlight

1. Click `Caixa`
2. Drag over the desired area

### Insert a text comment

1. Click `T`
2. Click anywhere on the page
3. Type the comment in the popup
4. Adjust size, bold, and italic
5. Click `OK`

### Save annotated PDF

- `Salvar como`: tries to open the system save picker so you can choose folder and filename
- `Download PDF`: downloads a timestamped copy

## Privacy

- PDFs are processed locally in the browser
- there is no backend in this project
- annotations are stored locally in the browser via `localStorage`

## Security Notes

- no tokens, secrets, private keys, or credentials were found in the local repository during review
- the project currently depends on public CDNs for `pdf.js` and `pdf-lib`
- for stricter production setups, consider vendoring these assets locally and adding integrity controls where possible

## Repository Files

- `index.html`: full application
- `README.md`: English documentation
- `README.pt-BR.md`: Brazilian Portuguese documentation
- `.gitignore`: public-repo exclusions
- `LICENSE`: project license

## Recommended GitHub Description

Dark-mode PDF reader with highlights, comments, search, zoom, print copy, and annotated PDF export — fully client-side.

## License

MIT
