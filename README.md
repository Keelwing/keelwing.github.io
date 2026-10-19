# keelwing.github.io

Keelwing's website, https://keelwing.github.io, and the brand files.

- `site/`: what GitHub Pages serves, as it is: `index.html` and `brand/`.
- [BRAND.md](BRAND.md): the mark, the colours, the type and the layer marks, and how to use them.
- [NAMING.md](NAMING.md): how repositories and packages are named (a proposal).

## Publishing

`.github/workflows/pages.yml` publishes `site/` on every push to main that changes it, or by hand. It needs GitHub
Pages on with GitHub Actions as its source (on a free plan, only for a public repository) and the repository
variable `PAGES_ENABLED` set to `true`. Until then the run is skipped.

To look at the site before that: `python3 -m http.server -d site`, then http://localhost:8000.
