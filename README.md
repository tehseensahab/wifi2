# WiFi Weekly

Hugo site for wifiweekly.com — router reviews, mesh guides, and connectivity news.

## Local preview

```
hugo server
```
Visit http://localhost:1313

## Add a post

```
hugo new content posts/my-post-slug.md
```
Front matter fields used by the templates:
- `title`, `date`
- `categories`: one of `reviews`, `news`, `guides`, `deals` (drives the nav + color swatch)
- `dek`: one-sentence subhead shown on cards and the hero
- `readtime`: e.g. `"6 min read"`
- `author`
- `weight`: any integer — only used to vary the card artwork pattern

## Deploy: GitHub + Cloudflare Pages

1. Push this folder to a new GitHub repo (e.g. `wifiweekly`).
2. In the Cloudflare dashboard: **Workers & Pages → Create → Pages → Connect to Git**, pick the repo.
3. Build settings:
   - Framework preset: **Hugo**
   - Build command: `hugo --minify`
   - Build output directory: `public`
   - Environment variable: `HUGO_VERSION` = `0.123.7`
4. Add the custom domain `wifiweekly.com` under the Pages project's **Custom domains** tab once the first deploy succeeds. If the domain is already on Cloudflare (as it should be, since you bought it there or added it as a zone), the DNS record is created automatically.
5. Every push to `main` redeploys automatically.

No GitHub Actions workflow is needed — Cloudflare Pages builds Hugo natively.
