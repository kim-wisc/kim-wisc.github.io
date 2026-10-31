# Design archive

Each folder holds the files that define one version of the site's look (templates, icons,
config). Content pages are not archived here — only design.

| Version | Date       | Look |
|---------|------------|------|
| v1.1.0  | 2026-10-30 | Original Lanyon: PT Serif/PT Sans, red (#ac4142) sidebar, text-only masthead, default favicon |
| v2.0.0  | 2026-10-30 | Kim Group brand: hexagon-lattice logo, Badger Red + Graphite, Manrope / IBM Plex Sans, brand.css |

## Roll back to v1.1.0

```bash
cp _archive/v1.1.0/_includes/head.html      _includes/head.html
cp _archive/v1.1.0/_includes/sidebar.html   _includes/sidebar.html
cp _archive/v1.1.0/_layouts/default.html    _layouts/default.html
cp _archive/v1.1.0/public/favicon.ico       public/favicon.ico
cp _archive/v1.1.0/public/apple-touch-icon-precomposed.png public/apple-touch-icon-precomposed.png
# then set  version: 1.1.0  in _config.yml
```
`public/css/brand.css`, `public/favicon-32.png` and `public/img/brand/` can stay; v1.1.0 templates never load them.

## Return to v2.0.0
Same commands with `_archive/v2.0.0/` as the source (also copies `public/css/brand.css`, `public/favicon-32.png`, `public/img/brand/`), and `version: 2.0.0`.

`_archive/drafts/` holds working files that were not adopted (e.g. a vector re-drawing of the logo).
