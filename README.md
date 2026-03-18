# Bridging Hearts Bereavement Support Group
## Website Prototype — GitHub Repository
**Date:** March 11, 2026
**Prepared by:** Claude (Anthropic) in collaboration with BYRNESZ

---

## 🌐 Live Site

This repository is published as a GitHub Page.
Once activated, the site will be available at:

```
https://yourusername.github.io/bridging-hearts-website/
```

> Replace `yourusername` and `bridging-hearts-website` with your actual GitHub username and repository name.

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `index.html` | Full 7-page website prototype — the GitHub Pages entry point |
| `README.md` | This document |
| `_config.yml` | GitHub Pages config — disables Jekyll so HTML loads as-is |
| `.nojekyll` | Prevents Jekyll processing of the site files |

---

## 🚀 Activating GitHub Pages

1. Push all files to your repository's **main** branch
2. Go to **Settings → Pages**
3. Under **Source**, select **Deploy from a branch**
4. Choose **main** branch, **/ (root)** folder → click **Save**
5. After 1–2 minutes your site will be live at the URL above

---

## About the Prototype

This is a fully functional single-file HTML prototype for the Bridging Hearts Bereavement Support Group website. It was built from the design criteria, copy, and SEO strategy developed collaboratively and refined interactively.

### Pages Included
1. **Home** — Hero section, trust strip, welcome/promise, three pillars, support groups highlight, testimonials, donation impact tiers
2. **About** — Organization story, mission statement, core values
3. **Support Groups** — What to expect, who can join, open invitation
4. **Resources** — Six topic cards including the *Group Activities & Events* card
5. **Get Involved** — Volunteer, partner, share your story, grant-maker section
6. **Donate** — Gift amount selector, donor form, impact breakdown
7. **Contact** — Message form, contact info, newsletter sign-up

---

## How to Open Locally

1. **Double-click** `index.html` — it will open in your default web browser
2. No internet connection required *except* to load Google Fonts (Cormorant Garamond + Nunito) — the site will still work offline but will fall back to system fonts
3. All navigation is fully functional — click any tab or button to move between pages

---

## Design Specifications

### Color Palette
| Name | Hex | Usage |
|------|-----|-------|
| Teal | `#3a7a74` | Primary brand, buttons, headings |
| Teal Light | `#5a9e97` | Hover states |
| Teal Pale | `#eaf4f3` | Backgrounds, highlights |
| Rose | `#c07b7b` | Accent, donate CTA, sticky button |
| Gold | `#c9a84c` | Impact numbers, accents |
| Cream | `#faf8f4` | Page background |
| Ink | `#2a2420` | Body text |

### Typography
- **Headings:** Cormorant Garamond (serif) — elegant, warm, trustworthy
- **Body:** Nunito (sans-serif) — friendly, readable, approachable

### Logo Mark
Custom SVG heart-bridge logo embedded directly in the HTML — no external image file needed.

---

## Placeholder Content to Replace

The following items need real details before going live:

| Location | Placeholder | Replace With |
|----------|-------------|-------------|
| Footer & Contact page | `info@bridgingheartsnh.org` | Confirm or update email |
| Contact page | Phone: "Available upon request" | Phone number (if desired) |
| Support Groups page | Meeting schedule TBD | Actual days/times/locations |
| Support Groups page | In-person/virtual options | Confirm format |
| Support Groups page | "Free or donation-based" | Confirm pricing model |
| Donate page | Donation form | Connect to payment processor (Stripe, PayPal, Zeffy) |
| Contact page | Contact form | Connect to form handler (Formspree, EmailJS) |
| Testimonials | Anonymous quotes | Real (anonymized) participant quotes |
| About page | Org origin story | Personal founding narrative |
| Footer | Social media buttons | Real social media links |

---

## The "Together & Connected" Button

On the **Resources page**, the *Group Activities & Events* card contains a **Together & Connected →** button that currently shows a placeholder alert. This is intentionally left as a stub for a future page.

**To activate it when ready:** A new "Together & Connected" page needs to be added to the site. Open a Claude session and request the build when ready.

---

## SEO Notes

Meta titles and descriptions are embedded in the `<head>`. For a live multi-page site, each page will need its own HTML file with unique meta tags.

**Primary keywords targeted:**
- grief support group
- bereavement support
- support after losing a loved one
- grief support groups near me *(add your NH region)*

---

## Next Steps

- [ ] Fill in all placeholder content (see table above)
- [ ] Build out the **Together & Connected** page
- [ ] Connect donation form to a payment processor
- [ ] Connect contact form to an email handler
- [ ] Add real testimonials (anonymized) as they become available
- [ ] Add NH regional location keywords for local SEO
- [ ] Set up Google Business Profile
- [ ] Migrate from prototype to a multi-page site when ready

---

*Bridging Hearts Bereavement Support Group — "We need not walk alone."*
