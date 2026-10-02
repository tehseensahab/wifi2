# WiFi Weekly

Hugo site for wifiweekly.com: reviews, guides, news, and deals for US home-network readers.

## Local preview

```
hugo server --buildFuture
```
Needs Hugo extended **v0.167.0 or newer** (webp image processing, `hugo.Data`).

## Structure

- **Content types** are sections: `content/reviews`, `news`, `guides`, `deals`. Each post is a folder (page bundle) with `index.md` and `cover.jpg`.
- **Topics** (the nine categories) are a taxonomy: `topics: ["mesh-wifi", ...]` in front matter. The first topic is the card label. Names, icons, descriptions, and order live in `data/topics.yaml`. Topic pages are `/topics/<slug>/`; Deals is its own section at `/deals/`.
- Static pages (About, Editorial policy, Corrections, Affiliate disclosure, Privacy, Terms, Contact) use `layout: static`.
- Author pages live at `/authors/<name>/`. Add each writer's role, bio and profile link in `data/authors.yaml` (empty fields are hidden).
- Other pages: How we test, WiFi glossary, a custom 404, and app icons (`static/favicon.svg`, `apple-touch-icon.png`, `site.webmanifest`).
- Internal Markdown links to posts that aren't published yet (scheduled or draft) render as plain text until the post goes live, so readers never hit a 404.
- Search is client-side: Hugo writes `/index.json` and `/search/` filters it. No build step needed.

## Add a post

```
hugo new reviews/my-review      # or guides/, news/, deals/
```
Add `cover.jpg` to the new folder. Front matter is documented in `archetypes/`. Key fields: `description` (one line for cards), `summary` (2-3 sentence answer-first box), `authors` (e.g. `["Dana Okafor"]`, links to their author page), `topics`, `imageAlt`, `faq`, `sources`. Reviews add `score`, `bestFor`, `testedOn`, `price`, `pros`, `cons`, `specs`. Set `lastmod` when you update an article; it shows as "Last updated".

Cover images: see `COVER-IMAGES.md`.

## Before launch

- Newsletter: set `params.newsletter.action` in `hugo.toml` to your provider's form URL. Until then the form is disabled.
- Confirm `params.contactEmail` (`hello@wifiweekly.com` is a placeholder).
- Review the Privacy and Terms pages with a lawyer.
- Read the How we test page and edit it so it matches exactly how you test.
- Fill in `data/authors.yaml`.
- The two review covers are generic router photos; replace them with photos of the actual products.
- Posts marked `sample: true` (and review scores marked `PLACEHOLDER`) are sample content. Replace with your real test data.
- Re-verify the source links in the sample posts.

## Deploy: GitHub + Cloudflare Pages

- Framework preset: Hugo. Build command: `hugo --minify`. Output: `public`.
- Environment variable: `HUGO_VERSION` = `0.167.0`.
- `static/_redirects` 301s the old `/posts/...` and `/categories/...` URLs to the new ones.
- `.github/workflows/daily-rebuild.yml` triggers a daily deploy hook so future-dated posts go live (needs the `CF_DEPLOY_HOOK` secret).
