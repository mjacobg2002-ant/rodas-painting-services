# Home-Service Website Template

A single-file, mobile-first, conversion-focused website template for **landscaping, concrete, and exterior/home-service** contractors. Built to be cloned and rebranded in ~5 minutes — change colors, drop in a logo and photos, find-and-replace the business details, done.

Distilled from real client sites (Sergio's Concrete, M León Landscaping, etc.) into one reusable, niche-agnostic base.

---

## Why it converts

- **Above-the-fold clarity** — headline, subhead, "Free Estimate" button, and a click-to-call phone number, all visible on first paint.
- **Phone number everywhere** — sticky top nav, hero, contact section, footer, and a **sticky mobile call/estimate bar** fixed to the bottom of the screen on phones (where most local-service traffic is).
- **Trust fast** — stats bar, "Why Us" grid, real reviews with stars, and a service-area section for local SEO.
- **One clear action** — every section funnels to "Get a Free Estimate" or "Call Now."
- **Fully responsive** — 3-column desktop layouts collapse cleanly to 1 column on mobile; hamburger menu; tap-friendly targets.
- **Fast & self-contained** — one HTML file, no build step, no frameworks. Just Google Fonts + inline SVG icons.
- **SEO-ready** — semantic HTML, meta/Open Graph tags, and LocalBusiness structured data.
- **Accessible** — skip link, focus states, ARIA labels, respects reduced-motion.

---

## Setup (5 minutes)

### 1. Copy the folder
Duplicate this folder and rename it for the new client (e.g. `green-valley-landscaping`).

### 2. Find-and-replace the tokens
Open `index.html` and Replace-All these placeholders:

| Token | Example |
|---|---|
| `{{BUSINESS_NAME}}` | Green Valley Landscaping |
| `{{TAGLINE}}` | Landscaping & Lawn Care |
| `{{PHONE}}` | (703) 555-0100 |
| `{{PHONE_TEL}}` | +17035550100 (digits only) |
| `{{CITY}}` | Fairfax |
| `{{REGION}}` | Northern Virginia |
| `{{STATE}}` | VA |
| `{{STREET}}` | 123 Main Street |
| `{{ZIP}}` | 22030 |
| `{{DOMAIN}}` | greenvalleylandscaping.com |
| `{{REVIEW_URL}}` | your Google review link |

### 3. Change the colors
In `index.html`, find the `★ BRAND COLORS` block near the top of the `<style>` and edit two lines:

```css
--accent:#1f8a4c;          /* main brand color */
--accent-bright:#28b264;   /* lighter hover version */
```

Presets are listed right below it — uncomment one:
- **Landscaping** (green): `#1f8a4c` / `#28b264`
- **Concrete** (steel blue): `#12a5db` / `#1cbdf0`
- **Roofing** (orange): `#e0632a` / `#f5793c`
- **Asphalt** (amber): `#d69a1e` / `#f0b02f`

### 4. Add the logo
Drop a transparent PNG at `images/logo.png` (~640×240). No logo yet? The business name shows as styled text automatically.

### 5. Add photos
Drop photos into `/images` using these names (any that are missing auto-hide and show a clean gradient, so the site never looks broken):

```
hero.jpg          about.jpg         cta-bg.jpg        area.jpg
service-1..6.jpg  gallery-1..9.jpg  step-1..4.jpg
residential.jpg   commercial.jpg
```

### 6. Edit the copy
Search `index.html` for `EDIT:` comments — those mark the headline, services, stats, reviews, and service-area text worth tailoring.

### 7. Make the form send (optional)
The form is a demo (shows a thank-you, sends nothing). Easiest fix: make a free [Formspree](https://formspree.io) form and set `<form action="https://formspree.io/f/YOUR_ID" method="POST">`, then delete the demo JS handler at the bottom. Or wire it to a GoHighLevel/CRM webhook.

---

## Deploy

Any static host works — it's just one HTML file plus an `images/` folder.

- **GitHub Pages:** push, then Settings → Pages → deploy from `main` / root.
- **Vercel / Netlify:** drag-and-drop the folder or connect the repo.

---

## Sections included

Nav (sticky) · Hero · Trust/stats bar · About · Services grid (6) · Keyword chips · Project gallery (masonry) · Process (4 steps) · Residential/Commercial split · Why Us · Reviews · Service Area · Contact form + details · Footer · Sticky mobile CTA.

Delete any section you don't want — each is a clearly commented `<section>`.
