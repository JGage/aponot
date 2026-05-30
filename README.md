# Denizen Healthcare — Website

Public-facing website for Denizen Healthcare, deployed to [denizenhealthcare.com](https://denizenhealthcare.com).

## Current state

Phase 1 holding page — single static `index.html`, no build process, no framework.

Will evolve into a real marketing site (multi-section landing page with team, advisor letter, contact form, etc.) in the next 2-4 weeks. Real-site build will likely add a framework (Next.js or similar) at that point.

## Local preview

```
open index.html
```

Or serve via any local web server (Python's built-in is fine for static):

```
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deployment

Auto-deployed to Vercel on push to `main`. Vercel project is configured for static file deployment (no build command, output directory = root).

## Domain

- Primary: `denizenhealthcare.com` → this project
- Held: `denizenhealth.com` (purchased separately as protective hold; not currently pointed)

## Structure

```
.
├── index.html      # Single-page holding site
├── .gitignore
└── README.md
```

When the real site lands, expect this to grow into a framework-based project structure (likely Next.js).
