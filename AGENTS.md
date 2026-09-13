# iTrain

A single-page static marketing/landing site for **iTrain** (an AI operations platform for personal trainers). It ships as plain `index.html` + `style.css` and is deployed via GitHub Pages (`.nojekyll` is present so the files are served as-is).

## Cursor Cloud specific instructions

- This is a **static site with no build step, no dependencies, no package manager, and no test/lint tooling**. The only tracked files are `index.html`, `style.css`, and `.nojekyll`. There is nothing to install; the update script is intentionally a no-op.
- **Run it in development** by serving the repo root over HTTP (the CSS is loaded via a relative path, so opening `index.html` via `file://` works too, but an HTTP server matches production most closely):

  ```bash
  python3 -m http.server 8000
  ```

  Then open `http://localhost:8000/`. Python 3 is already available in the environment. `python3 -m http.server` has no auto-reload — just refresh the browser after editing `index.html`/`style.css`.
- **Lint/test/build:** none exist. There is no CI build; GitHub Pages serves the files directly. If you add tooling, update this section.
- The page is interactive only via in-page anchor navigation (nav links smooth-scroll to `#platform`, `#how`, `#pilot`). The two CTA buttons are `mailto:` links, so clicking them opens an email client rather than navigating in-page.
