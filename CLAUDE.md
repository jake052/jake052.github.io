# Jake Buck — Personal Website

## What this project is

A personal professional website built with Hugo, hosted on GitHub Pages. Not a portfolio, not a blog platform, not a lead-gen tool. It's a strategic professional asset — the thing Jake sends in cover letters, LinkedIn messages, and email intros to make a better first impression than any CV could.

Jake is early-career and interdisciplinary: support worker → Business Innovation degree (first-class, 84% final year) → Health & Social Care Policy → MSc Data Science & Modelling. The through-line is turning fragmented human systems into coherent, actionable pictures. The site must make that through-line obvious.

---

## Who it's for

**Primary:** Hiring managers, MSc supervisors, and potential research collaborators evaluating whether Jake is worth a conversation. Time-poor, skim fast, judge in seconds.

**Secondary:** Peers and professionals in adjacent fields (care tech, public policy, data science) who might find Jake's writing useful.

**Not for (yet):** General public, coaching clients, event organisers, service buyers. These audiences may emerge; don't build for them now.

**The impression visitors should leave with:** *"Interesting, intelligent person — works across disciplines in a way that's rare and useful."* Not: *"Recent graduate looking for a job."*

---

## Stack

| Layer | Choice | Notes |
|-------|--------|-------|
| Generator | Hugo (extended) | Fast builds, no JS dependency, pure prose site |
| Hosting | GitHub Pages | Free, custom domain + HTTPS, auto-deploys on push |
| Domain | TBD (~£10/yr) | Cloudflare Registrar, Namecheap, or Porkbun |
| Content | Markdown in `content/` | |
| Styling | Custom CSS, no framework | Single file: `static/css/style.css` |
| Fonts | Cormorant Garamond (serif headings), Libre Franklin (sans body), IBM Plex Mono (mono/annotations) | Self-hosted for performance |
| Analytics | None (add later if wanted) | |
| Total cost | ~£10/year (domain only) | |

---

## Directory structure

```
jakebuck.com/
├── CLAUDE.md                    # This file
├── hugo.toml                    # Hugo config
├── content/
│   ├── _index.md                # Landing page
│   ├── projects/
│   │   ├── _index.md            # Projects listing
│   │   └── people-helping-people.md
│   ├── blog/
│   │   ├── _index.md            # Blog listing
│   │   └── *.md                 # Posts (added over time)
│   ├── experience.md
│   └── contact.md
├── layouts/
│   ├── _default/
│   │   ├── baseof.html          # Base template (head, nav, footer)
│   │   ├── single.html          # Single page/post
│   │   └── list.html            # Listing pages
│   ├── index.html               # Homepage template
│   └── partials/
│       ├── head.html            # <head> (meta, fonts, CSS)
│       ├── nav.html
│       └── footer.html
├── static/
│   ├── css/style.css            # All styles, one file
│   ├── fonts/                   # Self-hosted Google Fonts
│   ├── images/
│   └── CNAME                    # Custom domain for GitHub Pages
├── .github/workflows/
│   └── deploy.yml               # GitHub Actions: build + deploy
└── README.md
```

---

## Design system: "The Philosopher's Napkin"

Warm, literary, dry. Light mode = warm paper + ink + golden accent. Dark mode = lamplight-on-old-desk. Both modes carry subtle grain overlay and hand-drawn doodle energy.

### Colour tokens (light / dark)

| Token | Light | Dark |
|-------|-------|------|
| `--bg` | `#f0ebe0` | `#131211` |
| `--bg-raised` | `#e8e2d4` | `#1c1a18` |
| `--bg-surface` | `#e2dbd0` | `#242120` |
| `--text` | `#2b2924` | `#d4cfc5` |
| `--text-dim` | `#5c5750` | `#9a9488` |
| `--text-faint` | `#8a8377` | `#6a6359` |
| `--accent` | `#96643a` | `#c4956a` |
| `--accent-hover` | `#7a5028` | `#dbb48e` |

### Typography

- Headings: `Cormorant Garamond`, weight 300–400, large sizes, tight letter-spacing
- Body: `Libre Franklin`, weight 300, 16.5px base, 1.8 line-height
- Mono/annotations: `IBM Plex Mono`, weight 300, small sizes (0.65–0.75rem)

### Key design elements

- **Grain overlay:** Subtle SVG noise texture on `body::before`, varies by theme
- **Wobbly underline:** Hand-drawn SVG path under key phrases, animates in via stroke-dashoffset
- **Annotations:** Mono italic asides with left border, reduced opacity — dry editorial commentary
- **Doodle:** SVG diagram on landing page illustrating data fusion concept with sketch-like aesthetic
- **Theme toggle:** Fixed bottom-right, pill-style track with sun/moon icons
- **Animations:** `fadeUp` and `fadeIn` with staggered delays (`animate-d1` through `animate-d6`)
- **Max width:** 620px content column, centred

### Interaction patterns

- Links: accent colour, no underline by default, border-bottom on landing links
- Hover states: subtle colour shifts, padding-left nudge on list items
- Easter egg: `.dont-panic` in footer reveals "DON'T PANIC" on hover (Hitchhiker's Guide reference)

---

## Page goals

### Landing page
Establish who Jake is and why someone should care, in under 10 seconds. The through-line between care experience and data/systems thinking must read as one coherent direction, not two separate interests. Clear next action: read a project, read a post, or get in touch.

**Current hero copy:** *"I work on the problem of turning fragmented care data into decisions that actually help people"* — followed by context paragraph and annotation.

**Not:** A CV summary. A skills list. "I'm passionate about making a difference."

### Projects page
The credibility engine. Substitute for testimonials and client logos that an early-career person doesn't have. Each project answers: What problem? What approach? What did I learn?

**Centrepiece:** People Helping People data fusion project — presented as a walkthrough, not a document download. Must work for both technically literate visitors (rigour, architecture) and non-technical visitors (grounded in real problems).

**Not:** A portfolio of university assignments. A list of technologies used.

### Blog
The "interesting, intelligent person" signal sustained over time. Posts connect ideas across fields that don't usually talk to each other. Editorial lane: interdisciplinary synthesis.

**Cadence rule:** At least monthly, or don't launch the section. An empty blog is worse than no blog.

**Not:** Content marketing. Tutorials. "What I learned this week."

### Experience page
Frame background as coherent narrative, not chronological list. Support work = domain expertise. Academic trajectory = deliberate narrowing focus, not indecision.

**Not:** A reformatted CV. A timeline of every job.

### Contact page
Simple, low friction. Email link. No form, no booking widget, no newsletter signup (yet).

---

## Content & copy rules

1. **First person throughout.** The site speaks as Jake. Keep a third-person bio available for formal contexts.
2. **Copy before design.** Positioning statement and page narratives written before visual decisions.
3. **Show, don't list.** Projects page does the heavy lifting. Skills lists, technology badges, and competency matrices are banned.
4. **No empty sections.** Every page must be complete and maintained.
5. **Audience-first homepage.** Answers the visitor's question ("should I care?"), not Jake's ("how do I look impressive?").
6. **Tone:** Professional-warm. Not confessional, not casual, not corporate. Dry wit is welcome — the annotations and doodle carry personality.

---

## Key research findings (informing decisions)

These come from analysis of 18+ live personal websites (Dorie Clark, Seth Godin, James Clear, Paul Boag, Ali Abdaal, Tim Ferriss, Adam Grant, Brené Brown, etc.):

- **Newsletter-as-primary-CTA** is the dominant pattern for established professionals — but Jake has no audience yet, so this is deferred. Contact is the current primary CTA.
- **Audience specificity** is the clearest differentiator between sharp and generic sites. Jake's site speaks to evaluators (hiring managers, supervisors), not "everyone."
- **Paul Boag's model** (clear services, specific outcomes, named testimonials, substantial content) is most directly replicable for someone building from an earlier career stage.
- **Credibility stacking order** (observed across sites): named testimonials → logo bars → quantified achievements → awards → video. Jake substitutes project walkthroughs for testimonials — the work IS the proof.
- **Homepage patterns** fall into credential-led, product-led, or concept-led. Jake's is a hybrid: concept-led positioning ("the problem of fragmented care data") backed by credential context.
- **Anti-patterns to avoid:** buzzword positioning, "I do everything" sites, content deserts, over-designed/under-written, passive voice about pages, generic crossed-arms headshots.

---

## Hugo config summary

```toml
baseURL = "https://jakebuck.com"
languageCode = "en-gb"
title = "Jake Buck"

[params]
  description = "I work on the problem of turning fragmented care data into decisions that actually help people."
  author = "Jake Buck"
  email = "hello@jakebuck.com"

[permalinks]
  blog = "/blog/:slug/"
  projects = "/projects/:slug/"
```

---

## Front matter templates

### Blog post
```yaml
---
title: "Post Title"
date: 2026-06-04
slug: "post-slug"
description: "One sentence for meta tags and listing pages."
draft: false
---
```

### Project
```yaml
---
title: "Project Name"
date: 2026-06-04
slug: "project-slug"
description: "One sentence."
status: "complete"  # or "in-progress"
weight: 1           # Display order (lower = higher)
draft: false
---
```

---

## Content workflow

Jake describes what he wants → Claude edits markdown/templates/CSS → Jake reviews diff → pushes to main → GitHub Actions builds Hugo and deploys.

---

## Deployment

GitHub Actions on push to `main`: checkout → install Hugo extended → `hugo --minify` → deploy to GitHub Pages. Custom domain via CNAME file in `static/` + DNS CNAME record → `<username>.github.io`. HTTPS auto-provisioned via Let's Encrypt.

---

## Open decisions

1. **Domain name** — check availability
2. **Headshot** — does a suitable photo exist?
3. **Blog launch timing** — defer until 2–3 posts are written?

---

## Build sequence

1. ~~Write positioning statement + landing page copy~~ ✓
2. Write experience page narrative
3. Write People Helping People project walkthrough
4. Set up Hugo project (config, templates, CSS)
5. Build templates and styles
6. Set up GitHub repo + deployment pipeline
7. Configure custom domain
8. Launch blog (only when content exists)
9. QA across devices
