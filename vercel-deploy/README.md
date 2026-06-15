# Dayfold Website

A calm, beautiful website for Dayfold - time awareness, not productivity pressure.

🌐 **Live:** [dayfold.app](https://dayfold.app)

## About Dayfold

Dayfold helps you understand how a day actually unfolds: scheduled time, loose tasks, habits, birthdays, journal notes, roles, and the quiet space between them.

**Not a hustle app.** Not a stricter calendar. Dayfold gives you a calmer way to understand time, attention, roles, and the shape of a real day.

## Quick Start

### Local Development

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/dayfold-website.git
cd dayfold-website

# Open in your browser
open index.html
# or just drag index.html into your browser
```

### Deploy to Vercel

1. Push to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Click "New Project"
4. Import this repository
5. Vercel will deploy automatically

### Custom Domain

1. In Vercel dashboard, go to Settings → Domains
2. Add your domain (e.g., dayfold.app)
3. Update DNS records according to Vercel's instructions
4. Wait 24-48 hours for DNS to propagate

## Project Structure

```
.
├── index.html                 # Main website file
├── site/
│   └── dayfold-site.css      # Website styles
├── _ds/
│   └── tokens/               # Design system tokens
│       ├── fonts.css
│       ├── colors.css
│       ├── typography.css
│       ├── spacing.css
│       └── base.css
├── public/
│   └── assets/
│       ├── dayfold-icon.png
│       ├── og-card.png
│       └── screens/          # App screenshots
├── package.json              # Project metadata
├── vercel.json               # Vercel config
└── README.md                 # This file
```

## Technologies

- **HTML5** - Semantic markup
- **CSS3** - Modern styling with CSS variables
- **Design System** - Dayfold design tokens and typography

## Design System

This website uses the Dayfold Design System for consistent, beautiful styling:

- **Colors:** Warm, earthy palette (camel, clay, ochre, sage, lavender, etc.)
- **Typography:** Hanken Grotesk for body and UI
- **Spacing:** Generous, breathing layouts
- **Radius:** Soft, rounded corners
- **Shadows:** Warm, diffuse shadows for depth

## Content

- **Hero Section:** Call to action with stacked app screenshots
- **Product Overview:** Timeline-first philosophy
- **App Screens:** Gallery of real Dayfold app screens
- **Features:** Core pillars and spaces
- **Privacy & Design:** Philosophy behind the app

## Scripts & Interactivity

The site uses vanilla JavaScript with:
- Lucide icons (loaded from CDN)
- Smooth scrolling
- Interactive timeline demo
- Form submissions

## License

© 2026 Dayfold. All rights reserved.

## Contact

- **Email:** hello@dayfold.app
- **Website:** dayfold.app

---

Made with care by the Dayfold team.
