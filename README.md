# buford.dev

Personal portfolio and blog built with [Astro](https://astro.build).

**Live at [buford.dev](https://buford.dev)**

## Tech Stack

- **Framework:** Astro 6 with TypeScript
- **Content:** Markdown & MDX via Astro Content Collections
- **Styling:** Scoped CSS with custom properties (light/dark theme)
- **Deployment:** GitHub Actions → rsync to Hetzner VPS (Caddy)
- **Extras:** RSS feed, sitemap, Open Graph meta, image optimization via Sharp

## Development

```sh
npm install
npm run dev       # localhost:4321
npm run build     # production build to ./dist/
npm run preview   # preview production build locally
```

## Deployment

Pushes to `main` trigger a GitHub Actions workflow that builds the site and deploys via rsync over SSH to the VPS.
