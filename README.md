# cleantest-1778334475-site

> White-label marketing site scaffold for **CleanTest**. v0 — awaiting brand spec from Graphic Designer.

## Stack

- [Astro](https://astro.build) v5
- [Tailwind CSS](https://tailwindcss.com) v4
- Deployed to [Cloudflare Pages](https://pages.cloudflare.com)

## Getting started

```bash
npm install
npm run dev
```

## Placeholder content

All placeholder copy is marked with `[PLACEHOLDER: ...]` comments throughout:

- `src/layouts/Base.astro` — page `<title>`, meta description, site URL, OG image
- `src/pages/index.astro` — all hero / features / CTA / footer copy and links
- `src/styles/brand-tokens.css` — neutral palette; Graphic Designer to replace in v1

## Deploy

Pushing to `main` triggers a production deploy via `.github/workflows/deploy.yml`.
Pull requests get Cloudflare Pages preview deploys automatically.

### Required GitHub secrets

| Secret | Where to get it |
|---|---|
| `CLOUDFLARE_API_TOKEN` | Cloudflare → My Profile → API Tokens → Create Token (use the **Edit Cloudflare Workers** template or a custom token with Pages write) |
| `CLOUDFLARE_ACCOUNT_ID` | Cloudflare → Overview (right sidebar) |

### First-time Cloudflare Pages setup

Create a Pages project before the first deploy:

```bash
npx wrangler pages project create cleantest-1778334475-site
```

Or create via the Cloudflare dashboard under **Workers & Pages → Create application → Pages → Connect to Git** (but skip the Git connection — use the GitHub Actions workflow instead).
