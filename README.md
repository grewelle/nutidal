# Okeke LLC Website

**Live URL:** https://okeke.us
**Stack:** Static HTML/CSS/JS
**Hosting:** Azure Static Web Apps

---

## Project Structure

```
okeke.us/
├── index.html                    # Homepage
├── styles.css                    # Global stylesheet
├── robots.txt                    # Search engine directives (incl. AI crawlers)
├── sitemap.xml                   # XML sitemap with lastmod dates
│
├── services/
│   ├── index.html                # Services page
│   └── services.css
│
├── research/
│   ├── index.html                # Research & Technology page
│   └── research.css
│
├── apps/
│   ├── index.html                # All Apps overview
│   ├── apps.css
│   ├── app-page.css              # Shared styles for individual app pages
│   ├── aircontrolla/index.html   # AirControlla landing page
│   ├── moviemaker/index.html     # Movie Maker landing page
│   └── scanprice/index.html      # ScanPrice landing page
│
├── about/
│   ├── index.html                # About page
│   └── about.css
│
├── contact/
│   ├── index.html                # Contact page
│   └── contact.css
│
└── Google-Business-Profile-Setup-Guide.docx  # SEO setup guide (can remove from deploy)
```

---

## Pages Overview

| Page | URL | Purpose |
|------|-----|---------|
| Homepage | `/` | Hero, services overview, featured apps, about preview |
| Services | `/services/` | Detailed service offerings (5 services) |
| Research | `/research/` | Technology focus areas and stack |
| Apps | `/apps/` | Portfolio of all published apps |
| About | `/about/` | Company story, values, expertise |
| Contact | `/contact/` | Contact info and methods |
| App Pages | `/apps/{appname}/` | Individual app landing pages |

---

## Features

### Design
- Clean, professional design with Inter font
- Light blue snowfall animation (respects `prefers-reduced-motion`)
- Fully responsive (mobile hamburger menu)
- Consistent navigation and footer across all pages

### SEO & Discoverability
- **Structured Data:** ProfessionalService schema on homepage
- **Open Graph & Twitter Cards:** Social sharing optimization
- **Sitemap:** XML sitemap with lastmod dates
- **robots.txt:** Explicitly allows all major AI crawlers:
  - Google (Googlebot, Google-Extended)
  - OpenAI (GPTBot, ChatGPT-User)
  - Anthropic (Claude)
  - Microsoft (Bingbot)
  - Perplexity, Meta, Apple, and more
- **Canonical URLs:** Trailing slash consistency

### Accessibility
- Semantic HTML structure
- ARIA labels on interactive elements
- Alt text for images
- Keyboard navigable

---

## App Store Integration

App icons are loaded directly from Apple's CDN (mzstatic.com). To update:

### Your App IDs
| App | App ID |
|-----|--------|
| AirControlla | 6467008935 |
| Movie Maker | 6755254508 |
| ScanPrice | 6755891772 |
| Mini Business Manager | 6502629041 |
| .Scroll | 6737844498 |
| PixelLearn | 6739592041 |

### Get Icon URLs
```bash
# Lookup any app
curl "https://itunes.apple.com/lookup?id=6755254508" | jq '.results[0].artworkUrl512'
```

---

## Customization

### Colors (styles.css)
```css
:root {
    --color-primary: #2563eb;    /* Blue accent */
    --color-text: #1a1a1a;       /* Dark text */
    --color-bg-alt: #f8f9fa;     /* Light sections */
}
```

### Snowfall Animation
Located in each HTML file's `<script>` section:
- Color: `rgba(173, 216, 230, opacity)` (light blue)
- Particles: 100
- Disabled for `prefers-reduced-motion`

### Contact Info
Update in all pages if changed:
- Email: `contact@okeke.us`
- LinkedIn: `https://www.linkedin.com/company/okeke-llc/`

---

## Deployment

See `AZURE-DEPLOY.md` for full Azure Static Web Apps deployment instructions.

### Quick Deploy (GitHub)
1. Push to GitHub
2. Create Azure Static Web App
3. Connect repo, set app location to `/`
4. Auto-deploys on push to main

---

## Post-Launch Checklist

- [ ] Verify site at https://okeke.us
- [ ] Submit sitemap to Google Search Console
- [ ] Create Google Business Profile (see included guide)
- [ ] Set up Bing Webmaster Tools
- [ ] Add to LinkedIn company page
- [ ] Request reviews from clients

---

## Local Development

No build step required. Open any HTML file directly or use a local server:

```bash
# Python
python -m http.server 8000

# Node.js
npx serve .

# Then visit http://localhost:8000
```

---

## License

© 2026 Okeke LLC. All rights reserved.
