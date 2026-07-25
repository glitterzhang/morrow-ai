# Morrow AI

The parent site for Morrow AI's tools — a hub page linking out to each product
(CreatorHQ now, more on the way).

## Structure

```
morrow-ai/
├── index.html      # hub/portfolio homepage
├── privacy.html     # Morrow AI's own privacy page (products link to their own)
└── assets/          # favicon, apple-touch-icon, OG share image
```

Plain static HTML, no build step — deployed directly to Vercel (Framework preset "Other",
no build command, output directory `.`).

## Domain structure

- `morrowai.app` — this repo (the hub page)
- `creator.morrowai.app` — CreatorHQ, deployed from its own separate repo/Vercel project
- `career.morrowai.app`, `research.morrowai.app`, `data.morrowai.app`, `optimize.morrowai.app` —
  reserved for future products, not yet deployed

Each product is its own independent repo and Vercel project, given a `*.morrowai.app` subdomain
as a custom domain. This repo never proxies or rewrites to them — it just links out.
