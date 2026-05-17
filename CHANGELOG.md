# Bridging Hearts Bereavement Support Group
## Website Project — Session Notes & Changelog

> This document captures key decisions, changes, and outstanding items across all working sessions.
> Maintained as a companion to `README.md` for continuity between sessions and team onboarding.

---

## Session Log

---

### Session 1 — Website Prototype Build
**Tool:** ChatGPT
**Output:** Design brief, sitemap, page-by-page copy, visual theme, SEO strategy

Key decisions made:
- **7-page structure** established: Home, About, Support Groups, Resources, Get Involved, Donate, Contact
- **Brand palette** selected: Teal `#3a7a74`, Rose `#c07b7b`, Gold `#c9a84c`, Cream `#faf8f4`
- **Typography** chosen: Cormorant Garamond (headings) + Nunito (body)
- **Custom SVG heart-bridge logo** created — no external image files needed
- **Tagline** established: *"We need not walk alone."*
- SEO strategy defined with primary keywords: grief support group, bereavement support, support after losing a loved one, grief support groups near me

---

### Session 2 — Prototype Refinement & Bug Fix
**Tool:** Claude (Anthropic)
**Output:** `BridgingHearts_Website.html` — single-file HTML prototype

Key decisions made:
- Full 7-page prototype built from Session 1 specifications
- **Bug fixed:** `showPage is not defined` console error — function moved to `window` scope so inline `onclick` attributes always resolve
- **Resources page updated:** "Helping Grieving Children" card replaced with "Group Activities & Events" card per request
- New card text reviewed via **suggest-first workflow** — three options presented, **Option C selected** and implemented:
  > *"Science tells us that informal connection is powerful medicine. When group participants gather outside structured sessions, the bonds that form can meaningfully support both emotional and physical wellbeing."*
- **Together & Connected** button added to Resources page as a stub (placeholder alert) — future page to be built

---

### Session 3 — GitHub Pages Packaging
**Tool:** Claude (Anthropic)
**Output:** `BridgingHearts_Website_GitHub.zip`

Key decisions made:
- Website packaged for GitHub Pages deployment
- `index.html` created (copy of prototype) as GitHub Pages entry point
- `.nojekyll` added to prevent Jekyll processing
- `_config.yml` added to disable Jekyll theme interference
- `README.md` drafted with setup instructions, placeholder content table, and next steps
- **Deployment URL pattern:** `https://yourusername.github.io/bridging-hearts-website/`

---

### Session 4 — Responsive Design
**Tool:** Claude (Anthropic)
**Output:** `BridgingHearts_Website_Responsive_GitHub.zip`

**Problem solved:** Website was not responsive on mobile and tablet devices — navigation broke, grids overflowed, text was not readable on small screens.

Key changes made:

**Mobile Navigation — hamburger menu added**
- Desktop nav (> 900px): unchanged — all links visible in header
- Tablet/mobile (≤ 900px): nav links hidden, hamburger ☰ button appears
- Tapping hamburger opens a full-width slide-down drawer with all 7 page links
- Drawer closes on link tap, outside tap, or page change
- Donate link styled prominently in the mobile drawer

**Four responsive breakpoints implemented:**

| Breakpoint | Key Changes |
|---|---|
| ≤ 900px (tablet) | Hamburger nav, 2-column grids, hero goes single column |
| ≤ 600px (mobile) | All grids single-column, buttons stack full-width, reduced padding |
| ≤ 380px (small phone) | Typography scaled down, donation grid adjusts to 2 columns |

**Other mobile fixes:**
- Hero buttons stack vertically and go full-width on small screens
- Trust strip items stack in single column
- Impact tiers scroll horizontally on very small screens
- Footer columns collapse to single column
- Newsletter form stacks vertically
- Sticky help button resized for mobile

---

### Session 5 — PayPal Donation Integration
**Tool:** Claude (Anthropic)
**Output:** Updated `index.html` in `BridgingHearts_Website_Responsive_GitHub.zip`

**Decision:** PayPal hosted button + new tab approach chosen over embedded SDK or popup.

**Rationale:**
- No server required — works on static GitHub Pages
- Most reliable across all browsers and mobile devices
- PayPal handles all security, PCI compliance, and payment processing
- No PayPal account required for donors

**PayPal details:**
- **Button type:** PayPal hosted donate button
- **Hosted Button ID:** `WLH7PLQ9R3TFS`
- **Form action:** `https://www.paypal.com/donate`
- **Opens:** New tab (`target="_blank"`)

**Payment methods supported (handled by PayPal automatically):**
- Visa, Mastercard, American Express, Discover
- Venmo (verify enabled in PayPal Account Settings → Payment Preferences)
- PayPal balance
- Pay Later / Pay in 4

**Changes to Donate page:**
- First Name / Last Name / Email fields removed — PayPal collects these securely
- Amount buttons wired with `data-amount` attributes passed to PayPal via hidden form field
- **"Other"** amount reveals a custom input field — validated (≥ $1) before submission
- Button text updated to: *"💝 Complete Your Gift via PayPal"*
- Trust signals added below button: *Secured by PayPal · No PayPal account required · Every gift helps*

---

### Session 6 — Contact Email Integration
**Tool:** Claude (Anthropic)
**Output:** Updated `index.html` in `BridgingHearts_Website_Responsive_GitHub.zip`

**Contact email established:** `info@bridgingheartsbereavement.org`

**Three locations updated:**

| Location | Change |
|---|---|
| Contact page — Send Message button | Now collects name, email, message from form fields and opens visitor's email app with everything pre-filled |
| Contact page — info card email | Replaced obfuscated placeholder with live `mailto:` link styled in teal |
| Footer — Support column | Replaced obfuscated placeholder with live `mailto:` link |

**How the contact form works:**
- Visitor fills in name, email, and message
- Clicks "Send Message →"
- Their default email app opens (Mail, Outlook, Gmail, phone mail app) with To, Subject, and body pre-filled
- Works on desktop and mobile

**Known limitation — noted for future upgrade:**
The current `mailto:` approach requires the visitor to have an email app configured on their device. For a more robust solution, integrate a form handler:
- **Formspree** — free tier available, messages land directly in inbox, simple to add
- **EmailJS** — client-side email sending, no server needed, free tier available

---

## Outstanding Items

### Placeholder Content Still to Replace

| Location | Placeholder | Replace With |
|---|---|---|
| Support Groups page | Meeting schedule TBD | Actual days, times, and location |
| Support Groups page | In-person/virtual options | Confirm format |
| Support Groups page | "Free or donation-based" | Confirm pricing model |
| Donate page | Donation form | ✅ PayPal integrated (Session 5) |
| Contact page | Contact form | ✅ mailto integrated (Session 6) |
| Testimonials | Anonymous placeholder quotes | Real anonymized participant quotes when available |
| About page | Org origin story | Personal founding narrative |
| Footer | Social media buttons (f, in, tw) | Real social media profile links |

---

### Technical Upgrades — When Ready

| Item | Notes |
|---|---|
| **Contact form handler** | Replace `mailto:` with Formspree or EmailJS for direct inbox delivery without requiring visitor's email app |
| **Together & Connected page** | Resources page button currently shows placeholder alert — full page to be built when content is ready |
| **Google Analytics** | Add GA4 tracking tag to monitor visitor traffic and page engagement |
| **Local SEO** | Add NH regional keywords (Keene, Monadnock region) to page copy and meta tags |
| **Google Business Profile** | Set up for local search visibility |
| **Real testimonials** | Add anonymized participant quotes as they become available |
| **Multi-page architecture** | Current single-file prototype; when going fully live consider splitting into separate HTML files for proper SEO per page |

---

### Repository Structure

```
bridging-hearts-website/
├── index.html          # Full 7-page responsive website
├── README.md           # Setup and deployment guide
├── CHANGELOG.md        # This file — session notes and decisions
├── _config.yml         # GitHub Pages configuration
└── .nojekyll           # Prevents Jekyll processing
```

---

### GitHub Pages Activation

1. Push all files to **main** branch
2. Go to **Settings → Pages**
3. Source: **main** branch, **/ (root)** folder → **Save**
4. Live at: `https://yourusername.github.io/bridging-hearts-website/`

---

### Key Contacts & Accounts

| Item | Detail |
|---|---|
| Contact email | info@bridgingheartsbereavement.org |
| PayPal hosted button ID | WLH7PLQ9R3TFS |
| GitHub Pages URL | To be confirmed after repository creation |

---

*Bridging Hearts Bereavement Support Group — "We need not walk alone."*
*Document maintained across Claude (Anthropic) sessions — last updated May 2026*
