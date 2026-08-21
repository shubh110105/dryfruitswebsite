# Kesar & Co. — Premium Dry Fruits & Namkeen Website

A high-converting, mobile-first single-page website for a premium dry fruits and namkeen brand based in Lucknow. Built with vanilla HTML, CSS, and JavaScript — no frameworks, no dependencies (except Google Fonts).

---

## Live Preview

Open `index.html` in any modern browser to preview the site locally.

---

## Project Structure

```
kesar-co/
├── index.html       # Complete single-file website (HTML + CSS + JS)
└── README.md        # This file
```

All styles and scripts are embedded inside `index.html` for zero-dependency deployment.

---

## Features

### Sections
| # | Section | Purpose |
|---|---------|---------|
| 1 | Hero | Headline, tagline, product preview cards, stats |
| 2 | Why Choose Us | 6 trust-building feature cards |
| 3 | Product Showcase | 6 products with price, benefits, and WhatsApp order buttons |
| 4 | Video Section | 3 video placeholders (sourcing, packaging, reactions) |
| 5 | Corporate Gifting | Feature list + live inquiry form |
| 6 | Customer Reviews | 3 testimonials with name, role, and star rating |
| 7 | Offers & Discounts | 3 promo cards with tap-to-copy coupon codes |
| 8 | Referral Program | 4-step referral flow with rewards |
| 9 | Blog / Health | 3 article cards (Health, Gifting, Lifestyle) |
| 10 | FAQ | 6 accordion questions |
| 11 | Marketplace | Links to Meesho, Amazon, WhatsApp Direct |
| 12 | Payment Methods | UPI, Bank Transfer, COD, Invoice |
| 13 | Footer | Links, social icons, location, copyright |

### Conversion Features
- **Sticky WhatsApp button** — fixed bottom-right, animated bounce, collapses to icon on mobile
- **AI Chatbot** — keyword-aware bot with quick-reply chips; routes to WhatsApp for orders
- **Email capture popup** — triggers after 8 seconds; suppressed after first close via `localStorage`
- **Coupon code cards** — tap to copy codes (`FEST20`, `CORP30`, `REF50`) with toast confirmation
- **Corporate inquiry form** — collects name, company, phone, quantity, occasion, and message
- **WhatsApp deep links** — every CTA pre-fills a message in WhatsApp for frictionless ordering

### Design & UX
- Apple-inspired minimal luxury aesthetic
- `Cormorant Garamond` (display) + `DM Sans` (body) typeface pairing
- Gold (`#C9A96E`) accent on warm cream (`#FAF8F5`) base
- Glassmorphism cards on dark sections
- Scroll-triggered reveal animations via `IntersectionObserver`
- Floating hero badges with CSS keyframe animations
- Fully responsive — mobile-first breakpoints at 768px and 480px

---

## Customisation Guide

### 1. WhatsApp Number
Replace every instance of `919999999999` with your actual number (country code + number, no spaces or `+`):

```html
<!-- Find and replace all occurrences of: -->
wa.me/919999999999

<!-- Example for +91 98765 43210: -->
wa.me/919876543210
```

### 2. Brand Name
The site uses **Kesar & Co.** — search and replace to update:

```
Kesar & Co.  →  Your Brand Name
```

### 3. Product Images
Emoji placeholders sit inside `.product-img` and `.jar-card-img` divs. Replace with `<img>` tags:

```html
<!-- Before -->
<div class="product-img">🌰</div>

<!-- After -->
<div class="product-img">
  <img src="images/almonds.jpg" alt="Premium Almonds" style="width:100%; height:100%; object-fit:cover;">
</div>
```

### 4. Prices
Update prices directly in the HTML inside `.product-price` elements:

```html
<div class="product-price">₹299 <span>/ jar</span></div>
```

### 5. Popup Timing
Change the delay (milliseconds) before the email popup appears:

```js
// In the <script> block — default is 8 seconds
setTimeout(() => { ... }, 8000);
```

### 6. Marketplace Links
Replace `#` placeholders with your actual store URLs:

```html
<a href="https://www.meesho.com/your-store" class="market-btn" target="_blank">
<a href="https://www.amazon.in/your-store" class="market-btn" target="_blank">
```

### 7. FSSAI License
Update the license number in the footer:

```html
FSSAI Lic. No. XXXXXXXXXXXXXXX
```

### 8. Contact Email
Replace the placeholder in the footer:

```html
<a href="mailto:hello@kesarco.in">hello@kesarco.in</a>
```

### 9. Coupon Codes
Update codes in the `offer-code` divs and the `copyCode()` calls:

```html
<div class="offer-code" onclick="copyCode('YOUR_CODE')">YOUR_CODE — Tap to Copy</div>
```

### 10. Video Thumbnails
The three video cards link to WhatsApp by default. Replace `onclick` with an actual video link or embed:

```html
<!-- Replace onclick with a YouTube embed or video URL -->
<div class="video-thumb" onclick="window.open('https://youtube.com/watch?v=YOUR_ID')">
```

---

## Deployment

### Option A — Static Hosting (Recommended)
Upload `index.html` to any static host:

- [Netlify](https://netlify.com) — drag and drop the file
- [Vercel](https://vercel.com) — `vercel deploy`
- [GitHub Pages](https://pages.github.com) — push to a repo and enable Pages
- [Tiiny.host](https://tiiny.host) — instant free hosting for HTML files

### Option B — cPanel / Shared Hosting
Upload `index.html` to your `public_html` folder via FTP or File Manager. Rename to `index.html` if it isn't already.

### Option C — WhatsApp Bio Link
Host on Netlify/Tiiny, then paste the URL in your WhatsApp Business profile bio.

---

## SEO

The following meta tags are pre-configured in `<head>`:

```html
<meta name="description" content="Kesar & Co. – Premium dry fruits and namkeen in elegant glass jars...">
<title>Kesar & Co. — Premium Dry Fruits & Namkeen | Lucknow</title>
```

**Recommended additions before going live:**

```html
<!-- Open Graph (WhatsApp / Facebook previews) -->
<meta property="og:title" content="Kesar & Co. — Premium Dry Fruits & Namkeen">
<meta property="og:description" content="Elegant glass jars, same-day Lucknow delivery.">
<meta property="og:image" content="https://yourdomain.com/og-image.jpg">
<meta property="og:url" content="https://yourdomain.com">

<!-- Favicon -->
<link rel="icon" href="favicon.ico">
```

---

## Browser Support

| Browser | Support |
|---------|---------|
| Chrome 90+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Mobile Chrome/Safari | ✅ Full |

Uses standard Web APIs: `IntersectionObserver`, `navigator.clipboard`, `localStorage`.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Markup | HTML5 |
| Styling | CSS3 (variables, grid, flexbox, keyframes) |
| Scripting | Vanilla JavaScript (ES6+) |
| Fonts | Google Fonts — Cormorant Garamond, DM Sans |
| Icons | Unicode emoji |
| Dependencies | None |

---

## License

This project was built for **Kesar & Co.** and is intended for private commercial use. Do not redistribute or resell without permission.

---

*Built with care for Lucknow's finest dry fruits brand.*
