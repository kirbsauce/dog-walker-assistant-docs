# Dog Walker Assistant — Docs

Public documentation for [Dog Walker Assistant (DWA)](https://dwa.kirbsauce.com),
served via GitHub Pages at **[docs.kirbsauce.com](https://docs.kirbsauce.com)**.

## Contents

- [`index.md`](index.md) — site home / overview.
- [`WALKER.md`](WALKER.md) — Walker Guide.
- [`ADMIN.md`](ADMIN.md) — Admin Guide.

## Theme

The site uses a custom dark + amber theme matching the app — no gem-based Jekyll
theme. Branding lives in:

- `_layouts/default.html` — page shell (header, nav, footer).
- `assets/css/style.css` — palette and typography (mirrors the app's
  `src/index.css`).
- `images/paw-logo.svg` — the paw logo (`#F5A800`).

`_config.yml` applies the `default` layout to every page. Add a screenshot by
dropping a PNG in `images/` with the filename referenced in the guide.

## Local preview

```sh
bundle exec jekyll serve
```
