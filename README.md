# Magic Sand Sort — website

The support and privacy website for the **Magic Sand Sort** iOS game, built with
[Hugo](https://gohugo.io/) and published to GitHub Pages.

**Live URLs**

- Home: <https://cardoe.com/MagicSandSort/>
- Support: <https://cardoe.com/MagicSandSort/support/>
- Privacy: <https://cardoe.com/MagicSandSort/privacy/>

## Editing the site

All page text lives in Markdown files under `content/`. To change a page, edit
the file and commit — that's it. Pushing to `main` automatically rebuilds and
deploys the site (usually live within a minute or two).

| Page    | File                   |
| ------- | ---------------------- |
| Home    | `content/_index.md`    |
| Support | `content/support.md`   |
| Privacy | `content/privacy.md`   |

- To show a **Download on the App Store** button on the home page, paste the
  App Store link into `appStoreURL` at the top of `content/_index.md`.
- Colors and styling live in `static/css/style.css`.
- The header menu and support email are configured in `hugo.toml`.

## Previewing locally (optional)

Install Hugo, then run a live-reloading preview:

```sh
brew install hugo      # macOS
hugo server            # then open the URL it prints, e.g. http://localhost:1313/MagicSandSort/
```

To do a production build into `public/`:

```sh
hugo --minify
```

## How deployment works

`.github/workflows/hugo.yml` builds the site with Hugo and deploys it to GitHub
Pages on every push to `main`. The site's base path (`/MagicSandSort/`) comes
from `baseURL` in `hugo.toml`.

**One-time setup:** in the repo's **Settings → Pages**, set **Source** to
**"GitHub Actions"**.

> Note: this repo intentionally has **no `CNAME` file**. The `cardoe.com` custom
> domain is configured at the account level, and adding a `CNAME` here would
> redirect the whole domain to this one project.
