# piebru.github.io

Personal hub page for https://piebru.github.io/ — a GitHub **user site** served
from the root of this repository's `main` branch.

The landing page (`index.html`) is a single static file: no JavaScript, no
build step, no external dependencies, no cookies. It follows the system
light/dark preference automatically.

## How to add a page

Open `index.html` and duplicate one `<li>` inside the matching category:

```html
<li>
  <a class="card" href="/your-page/">
    <span class="title">Your Page <span class="arrow" aria-hidden="true">→</span></span>
    <p class="desc">One-line description of the page.</p>
  </a>
</li>
```

Publish the page itself as a folder (e.g. `/your-page/index.html`) either in
this repo or as a separate repository shown under the same `piebru.github.io`
domain (like `/monotropism/`).

## How to add a category

Duplicate one `<section class="category">` block, give it a unique
`aria-labelledby` id, and (optionally) a color: add a
`.category.yourname { --cat: #rrggbb; }` rule next to the existing
`.health` / `.games` rules.

## Local preview

Any static server works, run from this directory:

```sh
uv run python -m http.server 8000
# then open http://localhost:8000/
```
