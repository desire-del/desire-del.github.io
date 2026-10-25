# soussou.

Personal research blog built with Quarto 1.10.19.

Published site: https://desire-del.github.io/soussou/

## Publish

Run from this directory:

```powershell
quarto render
quarto publish gh-pages --no-render --no-browser
```

The source branch is `master`; Quarto manages the `gh-pages` branch.
Check the rendered `_site/` before publishing. Never publish a preview rendered with `draft-mode: visible`.

Articles live in `posts/<slug>/index.qmd`. Keep unfinished articles marked `draft: true`.
The starter posts (`welcome`, `post-with-code`) and scientific fixture (`scientific-test`) are also excluded from project rendering and resources in `_quarto.yml`.
Remove an exclusion only when intentionally turning that fixture into a publishable article.

`_freeze/` preserves computational results; keep it in version control. `_site/` and `.quarto/` are generated and ignored.
The RSS feed is `index.xml`; an empty feed is expected until the first real article is published.