# MUSELIORA

Hebrew beauty, self and style magazine from Tiger Brands Global.

## Structure

- `site/data/articles/`: 70 sourced editorial articles in seven categories.
- `site/data/bunee.json`: the BUNEE ponytail article and verified offer.
- `site/assets/`: compressed editorial images. Attribution is on the Credits page.
- `site/build.mjs`: dependency-free static renderer.
- `dist/`: generated GitHub Pages website, including search, sitemap and article schema.

Build with Node.js 22 or later:

```sh
node site/build.mjs
```

Push to `main` to publish `dist` through GitHub Actions. The preview uses `noindex,follow` until its owner connects a permanent domain. No private investor demo, credentials, customer data or administrative tooling is included in this repository.

## Reader Systems

The Cloudflare backend provides signed visitor identities, genuine votes, daily deduplicated views, moderated comments/replies, deduplicated likes and privacy-limited engagement events. Comments are never automatically approved. The standalone Meta pixel requires marketing consent; Shopify retains its existing storefront pixel integration. The magazine does not emit Purchase events.

## Domain Launch

After ownership and DNS are verified:

1. Set `site/config.json` to the final HTTPS `siteUrl`, empty `basePath`, final `navigationUrl`, and `indexing: true`.
2. Add the exact final origin to the Worker's magazine CORS allowlist using the approved staging/production deploy process.
3. Add the verified domain to GitHub Pages, enable HTTPS and create `dist/CNAME`.
4. Rebuild, publish and validate every canonical, sitemap URL, share URL and Shopify navigation link.
5. Submit the new sitemap in Search Console. Keep the Shopify article duplicates hidden from search.

Structured data and `llms.txt` improve discoverability; they do not guarantee indexing or AI citations.
