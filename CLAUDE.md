# Watt — meta-landing page

This repo holds **only** the GitHub Pages source for the umbrella
landing page above the two sister desktop suites:

- CHasm (`isene/chasm`) — x86_64 asm
- Fe₂O₃ (`isene/fe2o3`) — Rust on `crust`

There is **no source code** here and there should never be. The
actual code lives in the member project repos.

## Layout

```
docs/
├── index.html       The page
├── style.css        Shared visual language with the two sister sites
└── img/
    ├── watt.svg     Hero logo (lightning bolt, gradient-fill)
    ├── chasm.svg    Copy of chasm/docs/img/chasm.svg
    └── fe2o3.svg    Copy of fe2o3/docs/img/fe2o3.svg
```

## GitHub Pages

Served from `master` branch, `/docs` path. Public URL:

- <https://isene.github.io/watt/>
- <https://isene.org/watt/> (via the apex CNAME on `isene.github.io`)

## When the sister logos change

If `chasm.svg` or `fe2o3.svg` is updated in their respective repos,
re-sync the copies here:

```bash
cp ../chasm/docs/img/chasm.svg docs/img/chasm.svg
cp ../fe2o3/docs/img/fe2o3.svg docs/img/fe2o3.svg
```

## Editing

- Keep the intro to **one paragraph**. The whole point of this page
  is that it's a portal, not another tools listing.
- The two doors are the centrepiece. Don't bloat them.
- Numbers strip: only update with measured idle figures from the
  actual machine the user runs (currently XPS 14, 70 Wh battery).
- Footer should link out to `isene.com`, `isene/watt`, and `github.com/isene`.

## Cross-link

`isene.github.io/_includes/navigation.html` should carry **one**
nav link — `Watt` — instead of two (CHasm and Fe2O3). The
detailed per-suite pages are reached *through* this page.
