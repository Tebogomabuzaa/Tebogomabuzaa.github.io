# tebogomabuzaa.github.io

Personal portfolio of Tebogo Jr Mabuza, hosted on GitHub Pages at **https://tebogomabuzaa.github.io/**.

It is a single static page (`index.html`) with no build step. Pages are switched with the URL hash:

| Page | URL |
| --- | --- |
| Home | `#/` |
| Projects | `#/projects` |
| A project case study | `#/projects/<slug>`, e.g. `#/projects/costcare` |
| About (certification, education, modules, skills) | `#/about` |

Images live in `img/`. Pushing to `main` publishes the site within a minute or two.

## Adding a project

1. Add the screenshots to `img/`, named `<slug>-<what>.png`.
2. In `index.html`, copy one of the `<div data-page="...">` case-study blocks (for example the CostCare one), change `data-page` to the new slug and update the content.
3. Add a row to the **Projects** list (`<ol class="plist">`). The project and "Live on AWS" counts on the home page are worked out from this list, so they update automatically. Give the row a `<span class="pill live">Live</span>` if the project is online.
4. Optionally add a card to **Featured projects** on the home page (`<div class="cards">`).
5. Update the **Previous / Next** links at the bottom of the neighbouring case studies.

## Previewing locally

```bash
python -m http.server 8000
```

Then open http://localhost:8000.
