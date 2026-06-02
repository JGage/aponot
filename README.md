# Denizen Healthcare — Website

Public-facing website for Denizen Healthcare, deployed to [denizenhealthcare.com](https://denizenhealthcare.com).

## Current state

Multi-page static site — no build process, no framework. Pages share `styles.css` for consistent styling.

## Pages

```
.
├── index.html             # Home / landing
├── how-it-works.html      # Detailed service walk-through
├── pricing.html           # Pricing + FAQ
├── sign-up.html           # Practice sign-up form
├── about.html             # About / story (placeholders for founder + team copy)
├── contact.html           # General contact form
├── resources.html         # Resource library (coming-soon stub)
├── privacy.html           # Privacy Policy (DRAFT — needs attorney review)
├── terms.html             # Terms of Service (DRAFT — needs attorney review)
├── hipaa-notice.html      # HIPAA Notice (DRAFT — needs attorney review)
├── styles.css             # Shared stylesheet
├── .gitignore
└── README.md
```

## Sign-up + contact forms

Both forms post to Formspree. To activate:

1. Sign up at [formspree.io](https://formspree.io) (free tier handles 50 submissions/month).
2. Create one form for sign-ups and (optionally) one for general contact.
3. Replace `YOUR_FORMSPREE_ID` in `sign-up.html` and `contact.html` with your actual endpoint ID.
4. Configure email notification settings in your Formspree dashboard.

Alternative options if you'd rather not use Formspree: Web3Forms (free, no signup), Netlify Forms (if hosting moves to Netlify), or a Vercel API route (requires adding a serverless function).

## Local preview

```
open index.html
```

Or serve via any local web server:

```
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deployment

Auto-deployed to Vercel on push to `main`. Vercel project is configured for static file deployment (no build command, output directory = root).

## Pre-launch checklist

Before going public with this site, finish these:

- [ ] Wire Formspree (or alternative) for the sign-up and contact forms
- [ ] Get Privacy Policy, Terms of Service, and HIPAA Notice reviewed by a licensed attorney
- [ ] Fill in founder story and team section in `about.html`
- [ ] Replace logo wordmark with a designed logo if/when one is ready
- [ ] Add `favicon.ico` and Apple touch icons
- [ ] Add an Open Graph image at `/og-image.png` (1200x630)

## Domain

- Primary: `denizenhealthcare.com` → this project
- Held: `denizenhealth.com` (purchased separately as protective hold; not currently pointed)

## Next iteration

If the marketing site needs more substantial functionality — multiple stories/articles, a CMS, gated content, dynamic forms — consider migrating to Next.js or Astro. The current static structure is plenty for the founding-25 phase.
