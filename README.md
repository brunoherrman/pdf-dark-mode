[English](./README.md) | [Português (Brasil)](./README.pt-BR.md)

<div align="center">

# PDF Dark Mode

Dark-mode PDF reader with highlights, comments, search, zoom, print copy, and annotated PDF export — fully client-side.

![Status](https://img.shields.io/badge/status-active-2ea44f?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-2563eb?style=for-the-badge)
![Made with](https://img.shields.io/badge/made%20with-Vanilla%20JS-f7df1e?style=for-the-badge)
![Client-side](https://img.shields.io/badge/runtime-browser-111827?style=for-the-badge)

[Download `index.html`](https://github.com/brunoherrman/pdf-dark-mode/raw/main/index.html) • [Open repository file](./index.html) • [Português (Brasil)](./README.pt-BR.md)

</div>

## Overview

PDF Dark Mode is a lightweight browser-based reader built for comfortable long reading sessions. It opens local PDFs, applies dark presets, supports annotations and styled text comments, and exports the annotated file without any backend.

## Why It Stands Out

- Entirely client-side: no server required
- Dark reading presets designed for different visual preferences
- Fast workflow for highlight, box annotation, and text comments
- Search with visible current-match emphasis
- Undo and redo support for safer annotation editing

## Feature Matrix

| Feature | Details |
|---|---|
| Dark presets | `Warm`, `Classic`, `Blue` |
| Navigation | Thumbnails, page jump, zoom, fit width, `100%` |
| Annotations | Text highlight, box highlight, text comments |
| Search | Match navigation with focused current result |
| Export | Save annotated PDF locally or download timestamped copy |
| Utilities | Copy current page as image, local persistence via `localStorage` |

## Quick Start

### Option 1: Open directly

Open `index.html` in the browser.

Notes:
- some browser APIs are limited under `file://`
- `Save as` works best when served from `localhost`

### Option 2: Recommended local server

```bash
python -m http.server 5500
```

Then open:

```text
http://localhost:5500
```

## How To Use

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

## Tech Stack

- HTML
- CSS
- Vanilla JavaScript
- [PDF.js](https://mozilla.github.io/pdf.js/)
- [PDF-lib](https://pdf-lib.js.org/)

## Privacy

- PDFs are processed locally in the browser
- there is no backend in this project
- annotations are stored locally in the browser via `localStorage`

## Security Notes

- no tokens, secrets, private keys, or credentials were found in the repository during review
- the project currently depends on public CDNs for `pdf.js` and `pdf-lib`
- for stricter production use, consider vendoring these assets locally and applying integrity controls where possible

## Known Limitations

- `Save as` depends on browser support for the File System Access API
- direct `file://` usage may limit some browser capabilities
- CDNs are required unless library files are bundled locally

## Repository Structure

- `index.html`: full application
- `README.md`: English documentation
- `README.pt-BR.md`: Brazilian Portuguese documentation
- `.gitignore`: public-repo exclusions
- `LICENSE`: project license

## Recommended GitHub Description

Dark-mode PDF reader with highlights, comments, search, zoom, print copy, and annotated PDF export — fully client-side.

## License

MIT
