# CLAUDE.md — Project Instructions for Claude Code

## What This Is

Marketing website for Capital Consulting Group (CCG), a Kenyan hospital financial rescue consultancy. Currently a single static HTML file that needs to be deployed and potentially enhanced.

## Key File

- `capital-consulting-group-v3.html` — The complete website. Self-contained HTML/CSS/JS with canvas animations.

## Design Principles (Non-Negotiable)

- **Aesthetic:** "Quiet noble drama" — institutional, modern, gravitas. Think BlackRock/McKinsey, not startup.
- **Never:** Teal colours (client has "teal PTSD"), stock imagery, hospital icons, stethoscopes, globes, handshakes, anything that looks like a generic consulting template.
- **Always:** Navy dominant palette, gold accents used sparingly, Cormorant Garamond for editorial content, Montserrat for UI elements.
- **The hero animation is critical** — crisis-to-control scroll transformation is the centrepiece. Don't simplify or remove it.

## Hero Animation Architecture

The hero is 200vh tall with a `position: sticky` canvas wrapper. Scroll progress (0→1) drives three visual phases:

1. **Crisis (sp 0-0.4):** Red/blue alternating ambulance glows with bright focal points + diffuse halos. Faint erratic EKG lines. Abstract corridor silhouettes. Dark vignette.
2. **Transition (sp 0.1-0.55):** Lights fade. EKG stabilises. Architectural grid appears.
3. **Control (sp 0.35-0.8):** Gold network nodes drift and connect. Clean structured navy.

Background is flat `rgb(15,31,53)` at all times to match the crisis section below — effects create mood on top of this base.

## Colour Variables

```css
--navy: #0A1628
--navy2: #0F1F35  /* Primary background — hero canvas + crisis section */
--gold: #D4A84B
--gold2: #E8C674
--cream: #F7F2EA
--cream2: #EDE5D4
--white: #FDFBF7
```

## Deployment Preferences

- Simple static hosting preferred (Vercel, Netlify, Cloudflare Pages)
- No build step needed for current version
- If converting to a framework, prefer Astro or plain Vite — avoid heavy frameworks
- Domain will likely be capitalconsulting.co.ke

## Form Backend

Contact form currently has `onsubmit="return false"`. Needs integration with one of:
- Formspree (simplest)
- Netlify Forms (if hosting on Netlify)
- Custom API endpoint

## Things to Add

- SEO meta tags + og:image
- Favicon (the "C/" mark)
- Analytics (Plausible preferred over Google Analytics for privacy)
- Possibly: Hospital Financial Health Scorecard (interactive 8-question tool, was prototyped in a React version)
