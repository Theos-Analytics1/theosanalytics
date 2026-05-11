# Theos Analytics — Official Website

**Business Intelligence & Strategic Research**  
26 Broadway, Manhattan, New York, NY 10004

---

## 🚀 Live Deployment

This site is built for **GitHub Pages** — zero backend required, fully static, production-ready.

### Deploy in 3 Steps

1. **Fork or upload** this repository to your GitHub account
2. Go to **Settings → Pages → Source → Deploy from branch → main / (root)**
3. Your site goes live at: `https://yourusername.github.io/theosanalytics`

### Custom Domain (e.g. theosanalytics.co)

1. Add a file named `CNAME` in the root containing just: `theosanalytics.co`
2. In your domain registrar (Namecheap / GoDaddy / Cloudflare), add these DNS records:
   ```
   Type: A    Name: @    Value: 185.199.108.153
   Type: A    Name: @    Value: 185.199.109.153
   Type: A    Name: @    Value: 185.199.110.153
   Type: A    Name: @    Value: 185.199.111.153
   Type: CNAME Name: www Value: yourusername.github.io
   ```
3. Enable **Enforce HTTPS** in GitHub Pages settings

---

## 📁 File Structure

```
theosanalytics/
├── index.html              ← Main website (all sections)
├── portfolio.html          ← Detailed portfolio & proposal
├── emails.html             ← Outreach email playbook
├── css/
│   └── theme.css           ← CSS variables & overrides
├── js/
│   └── main.js             ← All JavaScript interactions
├── assets/
│   └── favicon.svg         ← Brand favicon
├── CNAME                   ← Custom domain (edit this)
├── sitemap.xml             ← SEO sitemap
├── robots.txt              ← Search engine config
└── README.md               ← This file
```

---

## ✏️ How to Edit Content

### Change company name or contact details
Search for these strings in `index.html` and replace:
- `hello@theosanalytics.co` → your real email
- `26 Broadway, Manhattan` → your address
- `theosanalytics.co` → your domain

### Change colours (brand palette)
Open `css/theme.css` and edit the `:root` variables:
```css
:root {
  --electric: #2563eb;   /* Primary blue */
  --teal:     #0891b2;   /* Secondary teal */
  --gold:     #d97706;   /* Accent gold */
  --navy:     #0a1628;   /* Dark navy */
}
```

### Add/remove case studies
In `index.html`, find `<!-- CASE STUDIES -->` and duplicate or delete `.pb` blocks.

### Update pricing
Search for `$150`, `$750`, `$3,500` and update to your desired amounts.

### Update the proposal client name
In `portfolio.html`, find `Godrej Group` and replace with your client name.

---

## 🎨 Tech Stack

| Technology | Purpose |
|------------|---------|
| HTML5 | Structure & semantic markup |
| CSS3 (Custom Properties) | Advanced styling & animations |
| Vanilla JavaScript | Interactions, charts, scroll effects |
| SVG | All data visualisations & charts |
| Google Fonts | Syne + Inter + DM Mono |
| GitHub Pages | Free hosting & SSL |

**No frameworks. No dependencies. No build step required.**

---

## 📧 Making the Contact Form Work

The form currently shows a success animation only. To make it send real emails:

### Option A — Formspree (Free, recommended)
1. Go to [formspree.io](https://formspree.io) and create a free account
2. Create a new form and copy your endpoint URL
3. In `js/main.js`, find `handleSubmit()` and replace with:
```javascript
async function handleSubmit(e) {
  e.preventDefault();
  const form = e.target.closest('.form-grid');
  const data = new FormData(form);
  await fetch('https://formspree.io/f/YOUR_ID', {
    method: 'POST', body: data,
    headers: { 'Accept': 'application/json' }
  });
  // success handling...
}
```

### Option B — Netlify Forms
Deploy to Netlify instead of GitHub Pages and add `data-netlify="true"` to the form element.

---

## 🔍 SEO Setup

Edit these in `index.html` `<head>` section:
```html
<meta name="description" content="Your custom description here">
<meta property="og:title" content="Theos Analytics | ...">
<meta property="og:image" content="https://yoursite.com/assets/og-image.png">
```

Update `sitemap.xml` with your real domain before going live.

---

## 📱 Browser Support

- Chrome 90+ ✅
- Firefox 88+ ✅
- Safari 14+ ✅
- Edge 90+ ✅
- Mobile (iOS/Android) ✅

---

## 📞 Support

**Theos Analytics**  
hello@theosanalytics.co  
26 Broadway, Manhattan, New York, NY 10004

---

*Built for GitHub Pages · © 2026 Theos Analytics LLC*
