# Capital Consulting Group — Website

## Project Overview

Website for Capital Consulting Group (CCG), Kenya's first integrated financial rescue platform for private hospitals. Single-page marketing site built as a static HTML file, ready for deployment.

## Brand Identity

- **Name:** Capital Consulting Group
- **Wordmark:** CAPITAL / consulting group (slash separator, dead-centre aligned subtext)
- **Tagline:** "Financial clarity for hospitals that can't afford confusion."
- **Palette:**
  - Navy (primary): `#0A1628`
  - Navy 2 (backgrounds): `#0F1F35`
  - Gold (accent): `#D4A84B`
  - Gold light: `#E8C674`
  - Cream: `#F7F2EA`
  - Cream 2: `#EDE5D4`
  - White: `#FDFBF7`
- **Typography:**
  - Headlines/body: Cormorant Garamond (serif, 300/400 weight)
  - Labels/nav/buttons: Montserrat (sans, 400/500/600 weight)
- **Tone:** Institutional but modern. Quiet noble drama. Trust. Gravitas.

## Hero Animation — Crisis → Stabilisation → Control

The hero section is 200vh tall with a sticky canvas that transforms as the user scrolls:

### Initial State (no scroll):
- Navy2 background with alternating red/blue ambulance light glows (focal point + diffuse halo)
- Lights alternate on ~1.7s cycle (smooth sine crossfade, not hard blink)
- Faint EKG lines with crisis heartbeat waveform (16% opacity main, 9% secondary)
- Abstract hospital corridor silhouettes (right side)
- Vignette deepens edges during crisis state

### Scroll Transition:
- Red/blue glows fade out
- EKG stabilises from erratic to calm sine, then fades
- Architectural grid lines appear (right side only)
- Gold network nodes emerge and drift, connecting to nearby nodes

### Final State:
- Clean navy2 matching the crisis section below (seamless transition)
- Structured gold node network
- Calm, institutional feel

## Site Structure

1. **Hero** — Full-viewport scroll-driven animation with headline, tagline, CTAs
2. **Crisis** — Four stat cards with sourced data (KES 76B unpaid, 53% reimbursement, etc.)
3. **Services** — Four products in alternating left/right layout with watermark numbers
4. **How It Works** — Four-phase timeline grid (Diagnose → Fix → Build → Leave)
5. **For Whom** — Target customer profile (20-150 bed hospitals, doctor-founded)
6. **Quote** — The "KES 5M promise" pull quote
7. **Contact** — Split layout: details left, enquiry form right
8. **Footer** — Wordmark + tagline + copyright

## Files

- `capital-consulting-group-v3.html` — Complete website (single file, self-contained)

## Deployment Notes

- Static HTML — no build step required
- Google Fonts loaded from CDN (Cormorant Garamond + Montserrat)
- No external JS dependencies
- Mobile responsive (breakpoint at 900px)
- Form is front-end only — needs backend integration for submissions
- Contact details are placeholder — update phone number, email before launch

## What Needs Doing

- [ ] Deploy to hosting (Vercel, Netlify, or similar)
- [ ] Connect custom domain (capitalconsulting.co.ke or similar)
- [ ] Wire up contact form (Formspree, Netlify Forms, or custom backend)
- [ ] Replace placeholder phone number (+254 700 000 000)
- [ ] SSL certificate (automatic with most hosts)
- [ ] Add meta tags for SEO (og:image, description, etc.)
- [ ] Add favicon (use the C/ mark from the wordmark)
- [ ] Google Analytics or Plausible for tracking
- [ ] Optional: Convert to Next.js/Astro if you want a blog later
- [ ] Optional: Add the Hospital Financial Health Scorecard as an interactive tool

## Business Context

CCG is a bootstrapped consulting firm (5-person team, no salaries, commission-based) targeting Kenya's private hospitals (20-150 beds, KES 12-200M revenue). Four core products: Revenue Cycle Intelligence, Operational Margin Engineering, Credit & Liquidity Structuring, Clinical Quality as Financial Strategy. Performance-based pricing.

Full business model, financial projections, and research are in separate documents (not included in this repo).
