# Okener Enterprises

A lightweight, responsive landing page for [okener.com](https://okener.com), hosted with GitHub Pages. No dependencies or build step.

## Local preview

Run `python3 -m http.server 8000` in this directory, then open `http://localhost:8000`.

## Hosting

In the repository's **Settings → Pages**, select **Deploy from a branch**, branch **main**, folder **/ (root)**. Set the custom domain to `okener.com`, then enable **Enforce HTTPS** once the certificate is ready.

The `CNAME` file declares the custom domain. `.nojekyll` serves the static files directly.

## Cloudflare DNS

Use **DNS only** (gray cloud) for these records:

| Type | Name | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | okener.github.io |

Replace conflicting website records for `@` or `www`, preserving mail and verification records. GitHub redirects `www.okener.com` to `okener.com`.

See [GitHub's custom domain documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).
