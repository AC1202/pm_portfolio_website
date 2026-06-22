# Alvin Chen — PM Portfolio

**Live site → [alvin-chen.vercel.app](https://alvin-chen.vercel.app)**

A 2-page personal portfolio for a Product Manager, built from scratch using Claude Code in ~2–3 hours — no framework, no boilerplate, shipped straight to production.

---

## What's inside

| Page | Path | Description |
|---|---|---|
| About | `index.html` | Hero with quantified achievements, experience logo wall, bio + stat boxes, skill tags |
| Ventures | `ventures.html` | Real estate startup (image carousel), scuba diving, snowboarding |

---

## Tech Stack

### Frontend
- **Pure HTML5 / CSS3 / Vanilla JS** — zero framework, zero build step
- **CSS Grid** — 3-column hero bullet alignment, 2-column about layout
- **CSS custom properties** — single-source design tokens (colors, max-width, etc.)
- **Google Fonts** — Inter (300–700)
- **Vanilla JS carousel** — no library; prev/next + dot navigation, works for both image sets

### Deployment
- **Vercel CLI v54.2.0** — one-command production deploy (`vercel --prod --yes`)
- **Custom alias** — `vercel alias <deployment-url> alvin-chen.vercel.app`
- **Static hosting** — no server, instant global CDN

### Tooling
- **`npx serve`** — local preview server during development
- **Python 3 + `urllib`** — automated image scraping from a Wix-hosted site

---

## How I Built This with Claude Code

> I'm a PM, not an engineer. This entire codebase was written by [Claude Code](https://claude.ai/code) via natural language prompts. Here's what happened under the hood.

### Claude Code capabilities used

| Capability | What it did |
|---|---|
| `Read / Edit / Write` tools | Created and iteratively refined HTML/CSS/JS files |
| `Bash` tool | Ran shell commands — file copies, preview server, Vercel deploys |
| Python script generation | Wrote a urllib scraper to download images from a Wix site |
| CSS problem-solving | Solved 3-column bullet alignment using CSS Grid (`grid-template-columns: 1.25rem 190px 1fr`) |
| Vercel CLI automation | Ran `vercel --prod --yes` and `vercel alias` directly from the terminal |
| Iterative design refinement | Adjusted layout, typography, logo sizing, and section order based on feedback |

---

## Build Your Own

See [`PROMPT.md`](./PROMPT.md) — a reusable prompt template you can copy, fill in with
your own materials and taste, and hand to Claude Code to build *your own* portfolio.
You don't need to write any code.

---

## Project Structure

```
PM portfolio website/
├── index.html              # About / Home page
├── ventures.html           # Ventures page
├── assets/
│   ├── logos/              # Company logo files (JkoPay, Lazada, Alibaba, etc.)
│   ├── pics/               # Personal photos (headshot, scuba, snowboarding)
│   ├── decent/             # re_01.jpg – re_19.jpg (scraped renovation photos)
│   └── Alvin_Chen_Resume.pdf
├── README.md
└── PROMPT.md
```

---

## Design System

```css
--bg:       #FFFFFF
--bg-warm:  #F8F5F0   /* warm off-white sections */
--accent:   #C17B3B   /* warm amber — eyebrows, arrows, tags hover */
--text:     #111111
--muted:    #6B7280
--max:      960px     /* content max-width */
font-family: 'Inter', -apple-system, sans-serif
```

---

## Deploy Your Own

```bash
# 1. Clone the repo
git clone https://github.com/<your-username>/pm-portfolio.git
cd pm-portfolio

# 2. Preview locally
npx serve -l 3000 .

# 3. Deploy to Vercel
vercel --prod --yes

# 4. Set a custom alias (optional)
vercel alias <deployment-url> your-name.vercel.app
```

---

© 2026 Alvin Chen · [linkedin.com/in/alvinchentw](https://www.linkedin.com/in/alvinchentw)
