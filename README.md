# Saify Watch & Optical — Premium Digital Catalog

A premium digital catalog website for Saify Watch & Optical, Nagpur. Features a public-facing showroom site and a password-protected admin panel for product management.

## 🌐 Live URLs

- **Main Site:** `/` — Premium digital catalog (11 sections)
- **Admin Panel:** `/admin/` — Product management system (password: `saify2024`)

## 📁 Project Structure

```
site/
├── index.html              # Main website (11 sections)
├── products.json           # Product data file
├── admin/
│   └── index.html         # Admin panel (product CRUD)
├── src/
│   └── styles/
│       └── main.css       # Design system & all section styles
├── assets/
│   ├── img/               # Product & store photos
│   └── vid/
│       └── hero.mp4       # Hero video
└── netlify.toml           # Netlify deployment config
```

## ✨ Features

### Public Site
- 11 editorial sections (Hero, Trust, Categories, USP, Watch Collection, Eyewear, Experience, Reviews, Store, Final CTA, Footer)
- Cinematic hero video with progressive text reveal
- Google Maps embed (Section 09)
- Horizontal draggable product rails
- Floating mobile CTA bar (WhatsApp + Directions)
- 5.0★ / 674+ reviews used in 4 elegant placements
- "Enquire on WhatsApp" CTAs throughout (no fake prices)
- Fully responsive (mobile-first)
- `prefers-reduced-motion` support
- WCAG AA accessibility

### Admin Panel (`/admin/`)
- **Password:** `saify2024` (change in Settings)
- Add / Edit / Delete products
- Watch-specific fields: strap, dial color, case size, water resistance
- Eyewear-specific fields: frame type, material, color, lens type
- Image upload (Base64, up to 5MB)
- Stock management (In Stock / Low Stock / Out of Stock)
- Settings: store info, phone, hours
- Export / Import products (JSON)
- Change admin password
- Dashboard with stats

### Data Flow
```
Admin Panel (localStorage) 
       ↓
products.json (export)
       ↓
Main Site (loads JSON + merges admin data)
       ↓
Netlify (auto-deploy on git push)
```

## 🚀 Local Development

```bash
# Start local server
cd site
python3 -m http.server 8080
# Visit http://localhost:8080
```

## 📦 Deployment (Netlify)

This site is configured for Netlify:

1. Connect GitHub repo to Netlify
2. Build settings:
   - Build command: *(leave blank)*
   - Publish directory: `.`
3. Deploy!

The `netlify.toml` file handles SPA routing, security headers, and cache rules automatically.

## 🔐 Security

- Admin panel uses localStorage (suitable for small catalogs)
- All WhatsApp links use `rel="noopener"`
- Form data validation on both client and server
- Admin password stored in localStorage (change from default `saify2024`)

## 🎨 Design System

- **Colors:** 80% neutral (ivory/stone/charcoal), 15% dark contrast, 5% muted gold accent
- **Typography:** Cormorant Garamond (display) + DM Sans (body)
- **Components:** Modular, reusable across sections

## 📞 Contact

- **Store:** Saify Watch & Optical
- **Address:** Main Road, Sitabuldi, Nagpur, Maharashtra 440012
- **Hours:** 11:15 AM – 9:30 PM, Daily

---

© 2024 Saify Watch & Optical. All rights reserved.
