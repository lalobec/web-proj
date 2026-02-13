# Website Customization Checklist

Use this checklist to customize your website with your business information and branding.

## 🎯 Essential Customizations (Do First)

### 1. Business Information

- [ ] **Company Name**
  - [ ] Update page title in `index.html` (line ~13)
  - [ ] Update logo/brand name in navigation (line ~22)
  - [ ] Update footer company name (line ~380)
  - [ ] Update meta description (line ~5)

- [ ] **Contact Information**
  - [ ] Phone number: Replace `(555) 123-4567` throughout
  - [ ] Email: Replace `hello@craftply.com` throughout
  - [ ] Service area/location (line ~265)
  - [ ] Business hours in footer (line ~398)

- [ ] **Social Media Links**
  - [ ] Instagram URL (line ~404)
  - [ ] Facebook URL (line ~408)
  - [ ] Add other platforms if needed

### 2. Content & Copy

- [ ] **Hero Section** (lines ~40-55)
  - [ ] Update headline to match your value proposition
  - [ ] Rewrite subheadline
  - [ ] Update "500+ projects" badge (or remove)

- [ ] **Value Propositions** (lines ~60-95)
  - [ ] Customize the 3 value statements
  - [ ] Ensure they match YOUR differentiators

- [ ] **Services** (lines ~105-170)
  - [ ] Update kitchen services description
  - [ ] Update custom furniture description
  - [ ] Adjust service feature lists

- [ ] **About Section** (lines ~300-340)
  - [ ] Write your company story
  - [ ] Update years in business
  - [ ] Update number of projects
  - [ ] Add your philosophy/approach

- [ ] **Testimonials** (lines ~265-295)
  - [ ] Replace with real customer testimonials
  - [ ] Use actual customer names (with permission)
  - [ ] Add authentic project types

### 3. Visual Assets

- [ ] **Create images folder structure:**
  ```
  images/
  ├── hero/
  ├── services/
  ├── portfolio/
  └── about/
  ```

- [ ] **Replace placeholder images:**
  - [ ] Hero background (1920x1080px)
  - [ ] Kitchen service image (800x600px)
  - [ ] Custom furniture service image (800x600px)
  - [ ] 6 portfolio images (1200x900px each)
  - [ ] About section image (800x1000px)

- [ ] **Optimize all images:**
  - [ ] Compress to appropriate file sizes
  - [ ] Consider using WebP format
  - [ ] Add descriptive alt text

### 4. Brand Colors (Optional but Recommended)

- [ ] **Update CSS variables** in `styles.css` (lines ~3-12):
  - [ ] `--color-walnut`: Your primary brand color
  - [ ] `--color-forest`: Your dark accent
  - [ ] `--color-cream`: Background color
  - [ ] `--color-copper`: CTA/button color

## 🎨 Design Customizations (Optional)

### 5. Typography

- [ ] Change font family in `index.html` (line ~11)
- [ ] Update `--font-family` in `styles.css` (line ~25)
- [ ] Recommended: Keep Inter or choose similar sans-serif

### 6. Additional Sections

- [ ] Add more portfolio items
- [ ] Create case study pages (separate HTML files)
- [ ] Add FAQ section
- [ ] Add video section (YouTube embed)
- [ ] Add blog/news section

### 7. Form Customization

- [ ] **Contact Form** (lines ~355-390)
  - [ ] Add/remove form fields as needed
  - [ ] Update project type dropdown options
  - [ ] Customize success message

- [ ] **Form Backend Integration:**
  - [ ] Choose form service (Formspree, Netlify Forms, etc.)
  - [ ] Update form action in `script.js`
  - [ ] Set up email notifications
  - [ ] Test form submissions

## 🚀 Technical Setup

### 8. SEO & Analytics

- [ ] **Update meta tags** in `index.html`:
  - [ ] Meta description (line ~5)
  - [ ] Page title (line ~13)

- [ ] **Add Schema markup** (see README.md)
  - [ ] LocalBusiness schema
  - [ ] Include accurate business details

- [ ] **Add Google Analytics:**
  - [ ] Create GA4 property
  - [ ] Add tracking code to `index.html`

- [ ] **Add Open Graph tags** (for social sharing)
  - [ ] og:title
  - [ ] og:description
  - [ ] og:image (1200x630px)

- [ ] **Create additional files:**
  - [ ] `sitemap.xml`
  - [ ] `robots.txt`
  - [ ] `favicon.ico` (create and add to root)

### 9. Mobile Testing

- [ ] Test on iPhone (Safari)
- [ ] Test on Android (Chrome)
- [ ] Test tablet view (iPad)
- [ ] Verify hamburger menu works
- [ ] Check form usability on mobile
- [ ] Verify all buttons are tappable (44px minimum)

### 10. Cross-Browser Testing

- [ ] Chrome (latest)
- [ ] Firefox (latest)
- [ ] Safari (latest)
- [ ] Edge (latest)
- [ ] Check for layout issues
- [ ] Verify animations work

## 📊 Pre-Launch Checklist

### 11. Content Review

- [ ] Proofread all text for typos
- [ ] Verify all phone numbers and emails
- [ ] Check that all links work
- [ ] Ensure images have alt text
- [ ] Review for consistent tone/voice

### 12. Performance

- [ ] Run Google PageSpeed Insights
- [ ] Optimize images further if needed
- [ ] Minify CSS and JS (optional)
- [ ] Test loading speed on mobile

### 13. Legal & Compliance

- [ ] Add Privacy Policy page
- [ ] Add Terms of Service (if applicable)
- [ ] Update copyright year in footer
- [ ] Add cookie consent if needed (GDPR/CCPA)
- [ ] Include business license info if required

### 14. Conversion Optimization

- [ ] Verify CTA buttons are prominent
- [ ] Test form submission flow
- [ ] Add trust signals (certifications, awards)
- [ ] Ensure contact info is easily accessible
- [ ] Add "Click to Call" for mobile

## 🎉 Launch!

### 15. Deployment

- [ ] Choose hosting provider
- [ ] Upload files to server
- [ ] Configure domain name
- [ ] Set up SSL certificate (HTTPS)
- [ ] Test live site thoroughly

### 16. Post-Launch

- [ ] Submit sitemap to Google Search Console
- [ ] Submit to Bing Webmaster Tools
- [ ] Create Google My Business listing
- [ ] Set up Google Maps integration
- [ ] Share on social media
- [ ] Monitor analytics

### 17. Ongoing Maintenance

- [ ] Add new portfolio projects monthly
- [ ] Update testimonials regularly
- [ ] Monitor form submissions
- [ ] Review and update content quarterly
- [ ] Keep photos fresh and current
- [ ] Back up website regularly

## 📝 Quick Reference: File Locations

| What to Update | File | Line(s) |
|----------------|------|---------|
| Company Name | `index.html` | 13, 22, 380 |
| Phone Number | `index.html` | Search all |
| Email Address | `index.html` | Search all |
| Hero Headline | `index.html` | ~45 |
| About Story | `index.html` | ~310-325 |
| Testimonials | `index.html` | ~265-295 |
| Brand Colors | `styles.css` | ~3-12 |
| Fonts | `index.html` & `styles.css` | 11, 25 |
| Form Handler | `script.js` | ~115 |

## 💡 Tips for Success

1. **Start with content**: Get your text finalized before design tweaks
2. **Use real photos**: Invest in professional photography of your work
3. **Keep it simple**: Don't add features just because you can
4. **Test on real devices**: Simulators don't catch everything
5. **Get feedback**: Show to friends, family, potential customers
6. **Iterate**: Your website should evolve as your business grows

## ❓ Need Help?

- Check inline code comments
- Read the full `README.md`
- Search for tutorials on specific features
- Consider hiring a developer for complex customizations

---

**Once you complete this checklist, you'll have a professional, customized website ready to attract customers!**
