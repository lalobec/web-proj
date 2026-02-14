# Diseñoría - Sitio Web de Muebles a Medida

Un sitio web moderno y responsivo para un negocio de muebles de madera contrachapada a medida especializado en carpintería de cocina. Construido con HTML, CSS y JavaScript vanilla para un rendimiento óptimo y fácil personalización.

## 📋 Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
- [Customization Guide](#customization-guide)
- [File Structure](#file-structure)
- [Browser Support](#browser-support)
- [Performance Optimization](#performance-optimization)
- [SEO Recommendations](#seo-recommendations)
- [Deployment](#deployment)
- [Future Enhancements](#future-enhancements)

## ✨ Features

### Design & UX
- **Responsive Design**: Mobile-first approach that looks great on all devices
- **Modern UI**: Clean, professional design with warm color palette
- **Smooth Animations**: Subtle transitions and hover effects
- **Accessibility**: Semantic HTML, keyboard navigation, ARIA labels
- **Fast Loading**: Optimized images, minimal dependencies

### Sections
- Hero section with compelling call-to-action
- Value propositions highlighting key differentiators
- Services overview (Kitchens & Custom Furniture)
- Portfolio gallery with hover effects
- Process timeline (4 steps)
- Customer testimonials
- About section with company stats
- Contact form with validation
- Comprehensive footer

### Interactive Features
- Sticky navigation header
- Mobile hamburger menu
- Smooth scroll to sections
- Scroll-to-top button
- Active navigation highlighting
- Form validation
- Portfolio item interactions

## 🚀 Getting Started

### Option 1: Open Directly in Browser

1. Navigate to the project folder
2. Double-click `index.html` to open in your default browser
3. That's it! No build process required.

### Option 2: Use a Local Development Server

For better performance and to avoid CORS issues:

**Using Python:**
```bash
# Python 3
cd disenoria
python3 -m http.server 8000

# Visit: http://localhost:8000
```

**Using Node.js (http-server):**
```bash
npm install -g http-server
cd disenoria
http-server -p 8000

# Visit: http://localhost:8000
```

**Using VS Code Live Server:**
1. Install "Live Server" extension
2. Right-click `index.html`
3. Select "Open with Live Server"

## 🎨 Customization Guide

### 1. Update Business Information

#### Company Name & Logo
**File:** `index.html`

Find and replace all instances of "Diseñoría" with your business name:
```html
<!-- Line ~7 -->
<title>Your Business Name | Muebles de Madera a Medida y Cocinas</title>

<!-- Line ~18-22 -->
<div class="logo">
    <a href="#home">
        <img src="LOGO25.png" alt="Your Business Name" class="logo-image">
    </a>
</div>
```

#### Contact Information
**File:** `index.html` (Contact Section)

Update:
- Phone number: Search for `(555) 123-4567`
- Email: Search for `hola@disenoria.com`
- Service area: Search for "Área Metropolitana"
- Hours of operation

#### About Section
**File:** `index.html` (About Section)

Update:
- Years in business
- Number of projects completed
- Company story and philosophy

### 2. Change Color Scheme

**File:** `styles.css` (Lines 1-20)

Modify the CSS custom properties:
```css
:root {
    /* Your brand colors */
    --color-walnut: #8B6F47;      /* Primary wood tone */
    --color-forest: #2C3E2E;      /* Dark accent */
    --color-cream: #F5F1E8;       /* Background */
    --color-charcoal: #333333;    /* Text */
    --color-copper: #C77F4B;      /* CTA buttons */
}
```

### 3. Replace Images

The template uses Unsplash placeholder images. Replace them with your own:

**Hero Background:**
```html
<!-- File: styles.css, Line ~380 -->
background-image: url('images/hero-kitchen.jpg');
```

**Service Images:**
```html
<!-- File: index.html -->
<div class="service-image" style="background-image: url('images/kitchen-service.jpg');"></div>
```

**Portfolio Images:**
```html
<!-- File: index.html -->
<img src="images/portfolio/project-1.jpg" alt="Modern kitchen with custom cabinets">
```

**Recommended Image Sizes:**
- Hero: 1920x1080px (landscape)
- Service cards: 800x600px
- Portfolio: 1200x900px
- About: 800x1000px (portrait)

### 4. Update Copy/Text

All text content is in `index.html`. Key sections to customize:

- **Hero headline** (Line ~45): Your main value proposition
- **Hero subheadline** (Line ~46): Supporting text
- **Value propositions** (Lines ~60-90): Your key differentiators
- **Service descriptions** (Lines ~100-160): What you offer
- **Testimonials** (Lines ~250-290): Replace with real customer quotes
- **About section** (Lines ~300-330): Your company story

### 5. Customize Forms

**Contact Form Fields:**

To add/remove fields, edit `index.html` in the contact section:

```html
<div class="form-group">
    <label for="budget">Budget Range</label>
    <select id="budget" name="budget">
        <option value="">Select budget range</option>
        <option value="5000-10000">$5,000 - $10,000</option>
        <option value="10000-25000">$10,000 - $25,000</option>
        <option value="25000+">$25,000+</option>
    </select>
</div>
```

**Form Submission:**

Currently, the form displays a success message. To connect to a backend:

**File:** `script.js` (Line ~115)

Replace the `simulateFormSubmission` function:

```javascript
// Option 1: Use a form service (Formspree, Netlify Forms, etc.)
async function submitForm(data) {
    const response = await fetch('https://formspree.io/f/YOUR_FORM_ID', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(data)
    });
    return response.ok;
}

// Option 2: Use your own backend
async function submitForm(data) {
    const response = await fetch('/api/contact', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(data)
    });
    return response.ok;
}
```

### 6. Add Google Analytics

**File:** `index.html` (Before `</head>`)

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### 7. Add Social Media Links

**File:** `index.html` (Footer section)

Update the social media links:
```html
<div class="footer-social">
    <a href="https://instagram.com/yourbusiness" aria-label="Instagram">
        <!-- Instagram icon -->
    </a>
    <a href="https://facebook.com/yourbusiness" aria-label="Facebook">
        <!-- Facebook icon -->
    </a>
    <!-- Add more platforms: Pinterest, Houzz, etc. -->
</div>
```

## 📁 File Structure

```
disenoria/
├── index.html                      # Main HTML file (single-page app)
├── styles.css                      # All styling and responsive design
├── script.js                       # Interactive functionality
├── LOGO25.png                      # Company logo
├── README.md                       # This file
├── CLAUDE.md                       # Guide for Claude Code
├── CUSTOMIZATION_CHECKLIST.md      # Step-by-step customization guide
├── images/                         # Images organized by section
│   ├── hero/                       # Hero background images
│   ├── services/                   # Service card images
│   ├── portfolio/                  # Portfolio & project images
│   ├── about/                      # About section images
│   └── README.md                   # Image usage guide
└── proyectos/                      # Individual project detail pages
    ├── template-proyecto.html      # Template for new projects
    ├── cocina-moderna-minimalista.html  # Example project
    └── README.md                   # Instructions for adding projects
```

## 🌐 Browser Support

- ✅ Chrome (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

**Minimum Supported Versions:**
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## ⚡ Performance Optimization

### Current Optimizations

1. **No external dependencies**: Pure vanilla JavaScript, no libraries
2. **System fonts fallback**: Fast font loading
3. **CSS custom properties**: Efficient theming
4. **Debounced scroll events**: Better performance
5. **Lazy loading ready**: IntersectionObserver implemented

### Recommended Improvements

1. **Image Optimization:**
   ```bash
   # Use tools like ImageOptim, TinyPNG, or Squoosh
   # Target sizes:
   # - Hero: < 300KB
   # - Portfolio: < 150KB each
   # - Thumbnails: < 50KB
   ```

2. **Use WebP format:**
   ```html
   <picture>
       <source srcset="image.webp" type="image/webp">
       <img src="image.jpg" alt="Description">
   </picture>
   ```

3. **Minify CSS/JS for production:**
   ```bash
   # Use online tools or build tools
   # CSS: cssnano, clean-css
   # JS: terser, uglify-js
   ```

4. **Enable Gzip/Brotli compression** on your server

5. **Add caching headers:**
   ```
   Cache-Control: public, max-age=31536000  # For images
   Cache-Control: public, max-age=3600      # For HTML
   ```

## 🔍 SEO Recommendations

### Already Implemented

✅ Semantic HTML5 structure
✅ Meta description
✅ Descriptive alt text for images
✅ Heading hierarchy (H1-H4)
✅ Mobile-friendly design
✅ Fast loading

### Additional Recommendations

1. **Add Schema Markup (JSON-LD):**

```html
<!-- Add before </head> -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Diseñoría",
  "image": "https://yoursite.com/LOGO25.png",
  "description": "Carpintería de cocina y muebles personalizados de madera contrachapada",
  "@id": "https://yoursite.com",
  "url": "https://yoursite.com",
  "telephone": "(555) 123-4567",
  "email": "hola@disenoria.com",
  "priceRange": "$$",
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Your City",
    "addressRegion": "State",
    "postalCode": "12345",
    "addressCountry": "MX"
  },
  "openingHoursSpecification": {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
    "opens": "08:00",
    "closes": "18:00"
  }
}
</script>
```

2. **Create a sitemap.xml:**

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://yoursite.com/</loc>
    <lastmod>2026-01-01</lastmod>
    <priority>1.0</priority>
  </url>
  <!-- Add more pages if you create separate HTML files -->
</urlset>
```

3. **Add robots.txt:**

```
User-agent: *
Allow: /
Sitemap: https://yoursite.com/sitemap.xml
```

4. **Add Open Graph tags:**

```html
<!-- Add to <head> -->
<meta property="og:title" content="Diseñoría - Muebles de Madera a Medida y Cocinas">
<meta property="og:description" content="Carpintería de cocina y muebles personalizados construidos para durar.">
<meta property="og:image" content="https://yoursite.com/images/og-image.jpg">
<meta property="og:url" content="https://yoursite.com">
<meta property="og:type" content="website">
<meta property="og:locale" content="es_MX">
```

5. **Add Twitter Card tags:**

```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Diseñoría - Muebles a Medida">
<meta name="twitter:description" content="Carpintería de cocina personalizada construida para durar">
<meta name="twitter:image" content="https://yoursite.com/images/twitter-card.jpg">
```

## 🚀 Deployment

### Option 1: Static Hosting (Recommended)

**Netlify (Free):**
1. Create account at netlify.com
2. Drag and drop the `disenoria` folder
3. Done! Auto-deployed with HTTPS

**Vercel (Free):**
```bash
npm i -g vercel
cd disenoria
vercel
```

**GitHub Pages (Free):**
1. Create a GitHub repository
2. Push your code
3. Go to Settings → Pages
4. Select branch and save

### Option 2: Traditional Web Hosting

Upload files via FTP to your hosting provider:
- **Recommended hosts**: SiteGround, Bluehost, HostGator, DreamHost
- Upload all files to `public_html` or `www` folder
- Ensure `index.html` is in the root

### Option 3: WordPress Integration

If you want to integrate with WordPress:
1. Create a custom page template
2. Copy HTML sections into the template
3. Enqueue CSS and JS through `functions.php`
4. Use WordPress functions for dynamic content

## 🎯 Future Enhancements

### Phase 2 Features (Easy to add)

- ✅ **Project detail pages**: Individual pages for each portfolio item (IMPLEMENTED - see `/proyectos/` folder)
- **Blog section**: Add a news/project blog
- **Before/after slider**: Interactive comparison tool
- **Video testimonials**: Embed customer videos
- **Live chat**: Add Intercom, Drift, or Crisp

### Phase 3 Features (More complex)

- **Online quote calculator**: Estimate project costs
- **3D kitchen planner**: Interactive design tool
- **Client portal**: Login area for project tracking
- **CMS integration**: Use WordPress, Contentful, or Sanity
- **E-commerce**: Sell pre-designed furniture pieces

### Technical Improvements

- **Convert to Next.js/Gatsby**: For better SEO and performance
- **Add TypeScript**: Type safety for JavaScript
- **Component library**: React or Vue components
- **Design system**: Storybook for components
- **Testing**: Jest + Cypress for automated testing

## 📞 Support & Customization

Need help customizing the website?

1. **Check the code comments**: Extensive inline documentation
2. **CSS variables**: Easy theming via custom properties
3. **Modular JavaScript**: Each feature is self-contained

## 📄 License

This template is provided as-is for the custom furniture business. Feel free to modify and use as needed.

## 🎯 Additional Features

### Project Detail Pages
The site includes a complete system for creating individual project showcase pages:

- **Template system**: Copy `proyectos/template-proyecto.html` to create new projects
- **Example project**: `proyectos/cocina-moderna-minimalista.html` shows a complete implementation
- **Full documentation**: See `proyectos/README.md` for step-by-step instructions
- **SEO-friendly URLs**: Each project gets its own URL (e.g., `/proyectos/cocina-moderna.html`)

To add a new project:
1. Copy the template file
2. Fill in your project details and images
3. Link it from the main portfolio section

## 🙏 Credits

- **Design**: Custom design for Diseñoría
- **Icons**: Inline SVG icons (Feather Icons style)
- **Fonts**: Google Fonts (Inter)
- **Images**: Unsplash placeholders (replace with your own)

---

**Built with ❤️ for custom furniture craftsmen | Construido para artesanos del mueble a medida**
