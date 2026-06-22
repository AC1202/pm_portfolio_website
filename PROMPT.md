# Build Your Own Portfolio — A Reusable Prompt

This is the prompt I used to build this site with [Claude Code](https://claude.ai/code).
It's written as a **template you can copy and adapt** — swap in your own materials,
your own taste, your own story, and Claude will build *your* site, not a clone of mine.

The philosophy: **you bring the raw material and the direction; Claude handles the code.**
You don't need to know HTML. You do need to know what you want to say and roughly how it should feel.

---

## How to use this

1. Open Claude Code in an empty folder.
2. Drop in your assets (resume PDF, headshot, project photos, company logos).
3. Paste the prompt below, filled in with your own content.
4. Look at the result, then refine in plain language ("make the hero bigger", "this section feels empty", "reorder these"). Iteration is where the site actually gets good — see *Refinement* at the bottom.

---

## The Prompt Template

> Replace everything in `{{ }}` with your own content. Delete sections you don't need.

```
Build a {{2}}-page static portfolio website for me. Pure HTML / CSS / vanilla JS —
no framework, no build step. Deploy to Vercel when it's done.

## About me
{{ Paste your one-paragraph bio, or attach your resume PDF and say "pull my background from this." }}
Role / positioning: {{ e.g. Product Manager, Designer, Founder }}
The one-line message I want visitors to remember: {{ your tagline }}

## Materials I'm providing (in this folder)
- Resume:   {{ resume.pdf }}
- Headshot: {{ photo.jpg }}
- Logos:    {{ company logos for an experience wall }}
- Photos:   {{ any project / hobby photos }}

## Pages I want
1. Home / About — {{ hero + bio + key achievements + experience logos + skills }}
2. {{ second page, e.g. "Projects", "Ventures", "Work" }} — {{ what goes here }}

## Achievements to feature (give the numbers — they carry the page)
- {{ metric }} — {{ what you did, where }}
- {{ metric }} — {{ what you did, where }}
- {{ metric }} — {{ what you did, where }}

## Look & feel
- Tone: {{ e.g. "professional but with personality — not a boring resume site" }}
- Reference sites I like (match this level of craft, not the exact design):
  {{ https://kanesherwell.com  https://wjessewright.com  — or your own picks }}
- Color direction: {{ e.g. "warm, minimal, off-white background, one accent color" }}
- Font: {{ e.g. "clean sans-serif like Inter" }}

## Must-haves
- Contact: {{ mailto:you@email.com }}
- Links: {{ LinkedIn / GitHub / etc. }}
- Footer with copyright
- Mobile responsive

## If I need images from a website I own
{{ Paste the URL. Ask Claude to scrape the images and pull them into the project —
   it can write a script to do this even for JS-heavy sites like Wix. }}

Build it, then show me the result so I can give feedback before we deploy.
```

---

## Design Direction That Worked

Generic guidance you can hand to Claude — these are the choices that made this site feel
intentional rather than templated:

- **Single accent color.** One warm color used sparingly (eyebrow labels, link hovers, one highlighted word in the headline) reads more confident than a rainbow.
- **Quantified hero bullets.** Lead with numbers (`$560K GMV`, `150K+ stores`). A metric + one line of context beats a paragraph of adjectives.
- **Logo wall.** A row of recognizable company/school logos builds instant credibility. Keep them a consistent size and let them be colorful.
- **Generous whitespace, one narrow content column** (~960px max-width, centered). Restraint looks premium.
- **A second "human" page.** Side projects, hobbies, or ventures make you memorable. An image carousel here adds life without needing a backend.

---

## Reference Sites Worth Studying

The two sites I pointed Claude at for inspiration — clean, personal, PM/operator-style portfolios:

- [kanesherwell.com](https://kanesherwell.com/#about)
- [wjessewright.com](https://wjessewright.com/about)

Find 2–3 sites whose *feel* you want and give Claude the links. It reads the vibe, not the markup.

---

## Refinement — the part that actually matters

The first build is a starting point. The site got good through ~10 rounds of plain-language
feedback. Examples of the kind of notes that move it forward:

- "The achievement bullets don't line up — make the arrow, metric, and description into clean columns."
- "The logos are too small and grayscale — make them bigger and colorful."
- "Reorder these bullets so the story flows from business impact to technical depth."
- "The left side feels too heavy — rebalance it."
- "Add 'AI' to the headline if it fits, and tell me whether it actually improves it."

Tip: ask Claude to **evaluate your suggestions, not just execute them.** Telling it
"give me the pros and cons of each change" turns it into a design partner instead of a typist.

---

## Deployment (Claude does this for you)

```
vercel --prod --yes                              # deploy to production
vercel alias <deployment-url> your-name.vercel.app   # set a clean custom URL
```

That's the whole stack: a folder of files and the Vercel CLI. No framework, no server.
