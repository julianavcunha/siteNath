# siteNath

Portfolio website for designer Nathália Latini.

Published site: <https://julianavcunha.github.io/siteNath/>

## Project structure

- `html/` — homepage and portfolio pages. The homepage is `html/index.html`.
- `css/` — shared styles and page-specific styles in `css/derivados/`.
- `imagens/` — logos, social icons, flags, and portfolio images.
- `pdf/` — downloadable documents.

## Preview locally

From the repository root, start a local static server:

```powershell
py -m http.server 8000
```

Then open <http://localhost:8000/html/> in a browser. Stop the server with `Ctrl+C`.

The HTML pages reference CSS and images outside the `html/` directory. Make sure a deployment publishes those folders along with `html/`; publishing only `html/` would omit the referenced assets.

## Branch workflow

Keep `main` deployable. Start each change on a short-lived branch created from an up-to-date `main`:

```powershell
git switch main
git pull
git switch -c feature/short-description
```

Use `feature/` for new work, `fix/` for bug fixes, and `docs/` for documentation. Commit with a short, descriptive message, then push the branch and open a pull request. After merging, delete the branch.

## Commit messages

You do not need a long description for a small change. Say what changed in plain language:

```text
type: short description
```

Examples:

- `style: tighten spacing in the contact form`
- `content: correct a typo in the services page`
- `fix: update the Behance profile link`
- `docs: add local preview instructions`
- `chore: rename a portfolio image`

Use `style` for visual tweaks, `content` for page copy, `fix` for bugs, `docs` for documentation, and `chore` for maintenance. You can group a few related tiny edits into one commit; keep unrelated changes in separate commits.
