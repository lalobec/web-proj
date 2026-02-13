# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Diseñoría** is a static website for a custom furniture business specializing in kitchen cabinetry and plywood furniture. Built as a single-page application using vanilla HTML, CSS, and JavaScript with no build system or external dependencies (except Google Fonts).

**Language**: Spanish - all content, comments, and user-facing text are in Spanish.

## Development Commands

### Local Development

Start a local development server:

```bash
# Option 1: Python 3
python -m http.server 8000

# Option 2: Node.js (if http-server is installed globally)
http-server -p 8000
```

Then visit: http://localhost:8000

**Note**: No build process, bundler, or package manager is required. The site can also be opened directly in a browser by double-clicking `index.html`, though a local server is preferred to avoid CORS issues.

### Testing

No automated test suite exists. Testing is manual:
- Open the site in different browsers (Chrome, Firefox, Safari, Edge)
- Test responsive design at various viewport sizes
- Test mobile navigation toggle
- Test form validation and submission
- Verify scroll animations and sticky header behavior

## Architecture

### File Structure

```
/
├── index.html          # Complete single-page application
├── styles.css          # All styles with CSS custom properties
├── script.js           # Interactive features and form handling
├── LOGO25.png          # Company logo
├── README.md           # Comprehensive documentation
└── CUSTOMIZATION_CHECKLIST.md  # Customization guide
```

### Single-Page Application Pattern

The entire website exists in `index.html` as a single HTML document with multiple `<section>` elements:
- Hero section (#home)
- Values section (3 value propositions)
- Services section (#kitchens, #furniture)
- Portfolio section (#portfolio)
- Process section (#process)
- Testimonials section
- About section (#about)
- Contact section (#contact)
- Footer

Navigation uses anchor links (#) for smooth scrolling between sections.

### CSS Architecture

**CSS Custom Properties** (lines 4-51 in styles.css) control all theming:
- Brand colors: `--color-walnut`, `--color-forest`, `--color-cream`, `--color-copper`
- Spacing: `--space-xs` through `--space-xl` (8px base unit)
- Typography: Font sizes, line heights
- Transitions and shadows

**Responsive Design**: Mobile-first with breakpoints at:
- 640px (mobile)
- 1024px (tablet)
- 1440px (large screens)

### JavaScript Architecture

`script.js` handles all interactivity using vanilla JavaScript:
- **Mobile navigation**: Toggle hamburger menu (lines 14-43)
- **Sticky header**: Add/remove shadow on scroll (lines 46-62)
- **Smooth scrolling**: Anchor link navigation (lines 65-89)
- **Scroll-to-top button**: Visibility toggle (lines 92-111)
- **Active nav highlighting**: Track current section in viewport (lines 114-137)
- **Form validation**: Contact form handling (lines 140-236)
- **Portfolio interactions**: Click handlers (lines 239-254)
- **Lazy loading**: IntersectionObserver for images (lines 257-282)
- **Scroll animations**: Fade-in on scroll (lines 285-305)
- **Keyboard accessibility**: Focus trap in mobile menu (lines 308-334)

All scroll event handlers are debounced for performance (lines 337-354).

## Key Customization Points

### Brand Identity
- **Logo**: Replace `LOGO25.png` (currently 50px height on desktop, 40px on mobile)
- **Company name**: Search/replace "Diseñoría" throughout `index.html`
- **Colors**: Update CSS variables in styles.css:4-10

### Content Sections
- **Hero**: index.html:43-62 (headline, subheadline, CTA buttons)
- **Values**: index.html:64-100 (3 value propositions with icons)
- **Services**: index.html:102-140 (kitchen/furniture descriptions)
- **Portfolio**: index.html:142-197 (6 project cards with Unsplash placeholders)
- **Testimonials**: index.html:239-272 (3 customer testimonials)
- **About**: index.html:274-303 (company story, stats)
- **Contact**: index.html:305-382 (form and contact details)

### Contact Information
Search/replace throughout `index.html`:
- Phone: `(555) 123-4567`
- Email: `hola@disenoria.com`
- Service area: "Área Metropolitana"

### Form Handling
Currently, the form (script.js:142-192) uses a simulated submission with console logging. To connect to a backend:
1. Update `simulateFormSubmission()` function (script.js:173)
2. Replace with fetch() call to API endpoint or form service (Formspree, Netlify Forms)
3. Form validation is already implemented (email regex, required fields)

## Important Patterns to Maintain

### Accessibility
- Semantic HTML5 elements (`<header>`, `<nav>`, `<section>`, `<footer>`)
- ARIA labels on interactive elements (nav toggle, scroll-to-top button)
- Keyboard navigation support (Tab, Escape key handling)
- Focus trap in mobile menu
- Alt text on all images

### Responsive Design
- Mobile-first CSS approach
- Touch-friendly targets (minimum 44px on mobile)
- Hamburger menu for mobile (hidden on desktop)
- Fluid typography and spacing
- Grid layouts that collapse to single column on mobile

### Performance
- No external dependencies (except Google Fonts)
- Debounced scroll handlers
- IntersectionObserver for lazy loading
- CSS transitions over JavaScript animations
- Optimized image sizes (recommendations in README.md)

### Spanish Language
All text content is in Spanish. When adding new content:
- Maintain consistent tone (professional but approachable)
- Use formal "usted" form where appropriate
- Keep button text concise ("Solicita tu cotización", "Ver nuestro trabajo")

## Image Management

### Current Setup
All images use Unsplash placeholder URLs. For production:
1. Create `images/` directory structure:
   ```
   images/
   ├── hero/
   ├── services/
   ├── portfolio/
   └── about/
   ```
2. Replace Unsplash URLs with local paths
3. Recommended sizes (in README.md):
   - Hero: 1920x1080px
   - Services: 800x600px
   - Portfolio: 1200x900px
   - About: 800x1000px

### Image Optimization
- Compress images (target: <300KB for hero, <150KB for portfolio)
- Consider WebP format with fallbacks
- Add descriptive alt text in Spanish

## Form Integration

The contact form requires backend integration before deployment:

**Current behavior** (script.js:173-192):
- Simulates 1.5s network delay
- Shows success message
- Resets form
- Logs data to console

**To implement real submission**:
```javascript
async function submitForm(data) {
    const response = await fetch('https://formspree.io/f/YOUR_ID', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(data)
    });
    return response.ok;
}
```

## Browser Support

Targets modern browsers:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

Uses modern JavaScript features:
- IntersectionObserver
- async/await
- Arrow functions
- Template literals
- Spread operator

No polyfills or transpilation required for target browsers.

## Deployment

No build step required. Deploy by:
1. Upload all files to web server
2. Ensure `index.html` is in root directory
3. Configure SSL/HTTPS
4. Set up proper cache headers for images

Recommended static hosts (see README.md):
- Netlify (drag & drop)
- Vercel
- GitHub Pages
- Traditional web hosting (FTP upload)

## SEO Considerations

Currently missing (should add before deployment):
- `sitemap.xml`
- `robots.txt`
- Favicon (`favicon.ico`)
- Open Graph meta tags
- Twitter Card meta tags
- Schema.org JSON-LD (LocalBusiness markup)

Examples and recommendations are documented in README.md.

## Analytics Integration

Analytics code is stubbed but not implemented:
- CTA button tracking: script.js:373-381
- Portfolio view tracking: script.js:384-389

To enable, add Google Analytics 4 tracking code to index.html `<head>` and uncomment gtag() calls.

## Common Modifications

### Adding a New Section
1. Add `<section>` to index.html with unique `id`
2. Add corresponding styles to styles.css
3. Add navigation link to header (if needed)
4. Update smooth scroll logic if necessary

### Changing Colors
Update CSS variables in styles.css:4-10. Colors cascade throughout the entire site automatically.

### Adding Portfolio Items
Add `.portfolio-item` divs in index.html:149-191. Maintain the structure:
```html
<div class="portfolio-item">
    <img src="..." alt="...">
    <div class="portfolio-overlay">
        <h4>Título del proyecto</h4>
        <p>Descripción breve</p>
    </div>
</div>
```

### Modifying Form Fields
Edit form structure in index.html:345-378. Update validation logic in script.js:144-162 if adding/removing required fields.

## Maintenance Notes

This is a template/starter site with placeholder content:
- All testimonials are fictional
- All images are from Unsplash
- Contact information is placeholder data
- "500+ projects" badge should be updated with real numbers

Before going live, complete the customization checklist in `CUSTOMIZATION_CHECKLIST.md`.
