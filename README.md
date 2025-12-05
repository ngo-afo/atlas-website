# Atlas FinOps - QuickBooks Bookkeeping Landing Page

A professional, conversion-optimized landing page for Atlas FinOps QuickBooks bookkeeping services.

## 📋 Overview

This is a single-page marketing website designed to promote QuickBooks bookkeeping services for small businesses. The page is built to convert visitors into consultation calls or email leads.

## ✨ Features

- **Fully Responsive**: Mobile-first design that looks great on all devices
- **Modern Design**: Clean, professional aesthetic with Atlas FinOps branding (navy, white, soft gray)
- **Optimized for Conversion**: Clear CTAs, strong value propositions, and social proof
- **Fast Loading**: Minimal dependencies, optimized for performance
- **SEO Ready**: Complete meta tags, Open Graph, and Twitter Card tags included
- **Smooth Animations**: Subtle hover effects and scroll animations for engagement

## 🎨 Sections Included

1. **Hero Section** - Compelling headline with dual CTAs (Calendly + Email)
2. **How It Works** - 3-step process with icons
3. **Why Choose Atlas FinOps** - 6 key benefits in card format
4. **Services Overview** - What's included in the service
5. **Testimonials** - Social proof with 3 client testimonials
6. **Final CTA** - Repeat conversion opportunities
7. **Footer** - Copyright and link back to main site

## 🚀 Deployment Instructions

### Option 1: GitHub Pages (Recommended)

1. **Push to GitHub**:
   ```bash
   git init
   git add bookkeeping.html
   git commit -m "Add QuickBooks bookkeeping landing page"
   git branch -M main
   git remote add origin https://github.com/ngo-afo/atlas-website.git
   git push -u origin main
   ```

2. **Enable GitHub Pages**:
   - Go to your repository settings
   - Navigate to "Pages" section
   - Select "main" branch as source
   - Select "/ (root)" as folder
   - Click Save

3. **Access your page**:
   - The page will be available at: `https://atlasfinops.com/bookkeeping.html`
   - Or rename the file to `index.html` and deploy in a `/bookkeeping` folder for: `https://atlasfinops.com/bookkeeping/`

### Option 2: Direct Hosting

Simply upload `bookkeeping.html` to your web server in the desired directory:
- For `/bookkeeping` route: Create a `/bookkeeping` directory and rename file to `index.html`
- For `/quickbooks` route: Create a `/quickbooks` directory and rename file to `index.html`

### Option 3: Custom Domain Setup

If using a subdomain (e.g., `bookkeeping.atlasfinops.com`):
1. Upload `bookkeeping.html` and rename to `index.html`
2. Configure DNS CNAME record to point to your hosting
3. Update the `og:url` meta tag in the HTML to match your final URL

## 🔧 Customization Guide

### Set Up Formspree (REQUIRED)

The contact form uses Formspree to handle form submissions. Follow these steps:

1. **Create a Formspree account**:
   - Go to https://formspree.io
   - Sign up for a free account

2. **Create a new form**:
   - Click "New Form"
   - Name it "QuickBooks Bookkeeping Inquiries"
   - Copy your form endpoint (looks like `https://formspree.io/f/xzbqwxyz`)

3. **Update the form action** in `bookkeeping.html`:
   - Find line 599: `<form action="https://formspree.io/f/YOUR_FORM_ID"`
   - Replace `YOUR_FORM_ID` with your actual Formspree form ID

4. **Configure form settings** in Formspree dashboard:
   - Set notification email to `info@atlasfinops.com`
   - Customize the confirmation message
   - (Optional) Set up email notifications

**Email Address** (appears in hero and form):
```html
<a href="mailto:info@atlasfinops.com"
```
Replace with your preferred contact email if different.

### Update Main Website Link

In the footer CTA section:
```html
<a href="https://atlasfinops.com" class="text-white hover:text-blue-200 underline font-medium">
    Visit our main website →
</a>
```

### Update Colors

The color scheme is defined in the Tailwind config section:
```javascript
colors: {
    'atlas-navy': '#1e3a5f',
    'atlas-navy-light': '#2d4a6f',
    'atlas-navy-dark': '#162d47',
    'atlas-gray': '#f5f7fa',
    'atlas-gray-dark': '#e2e8f0',
}
```

### Update Content

All text content is easily editable directly in the HTML:
- **Headlines**: Look for `<h1>`, `<h2>`, `<h3>` tags
- **Body text**: Within `<p>` tags
- **Testimonials**: In the "Testimonials Section" (search for "What Our Clients Say")
- **Benefits**: In the "Why Choose Atlas FinOps" section

### Update Social Sharing Image (Optional but Recommended)

The **banner image** (also called Open Graph image) is what appears when someone shares your page on social media (Facebook, LinkedIn, Twitter, etc.).

Currently it's commented out in the HTML (line 17-18). To add one:

1. **Create a banner image**:
   - Recommended size: 1200px × 630px
   - Include your branding, headline, or key message
   - Use tools like Canva, Figma, or Photoshop
   - Example content: "Atlas FinOps - QuickBooks Bookkeeping | First 2 Months Free"

2. **Upload the image** to your website (e.g., `/assets/og-bookkeeping.jpg`)

3. **Uncomment and update line 17** in `bookkeeping.html`:
   ```html
   <meta property="og:image" content="https://atlasfinops.com/assets/og-bookkeeping.jpg">
   ```

Without this image, social media platforms will use a generic preview when your page is shared.

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🔍 SEO Checklist

- ✅ Meta title and description
- ✅ Open Graph tags (Facebook, LinkedIn)
- ✅ Twitter Card tags
- ✅ Semantic HTML structure
- ✅ Responsive viewport meta tag
- ✅ Fast load time (no external dependencies except fonts and Tailwind CDN)

**Before going live**, update:
- [ ] **CRITICAL**: Set up Formspree account and update form action URL (line 599)
- [ ] Verify email address `info@atlasfinops.com` is correct throughout the page
- [ ] Update the `og:url` meta tag with your final URL (line 16)
- [ ] (Optional) Create and add Open Graph banner image (1200x630px)
- [ ] Test the contact form submission to ensure you receive emails

## 📊 Analytics (Optional)

To add Google Analytics, insert before the closing `</head>` tag:

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

## 🎯 Conversion Optimization Tips

1. **Set up Formspree** and test form submissions thoroughly
2. **Test on mobile** - most traffic will be mobile
3. **Add real testimonials** - replace placeholders with actual client feedback
4. **Create a banner image** for social sharing (1200x630px) - increases click-through from social media
5. **Set up conversion tracking** (Google Analytics) to measure form submissions
6. **A/B test headlines** to improve conversion rates
7. **Monitor form spam** - Formspree has built-in spam protection, but monitor submissions
8. **Respond quickly** - aim to respond to inquiries within 24 hours as promised on the page

## 📝 File Structure

```
Website/
├── bookkeeping.html    # Main landing page (self-contained)
└── README.md          # This file
```

## 🆘 Support

For questions or issues:
- Email: info@atlasfinops.com
- GitHub Issues: https://github.com/ngo-afo/atlas-website/issues

## 📄 License

© 2024 Atlas FinOps. All rights reserved.

---

**Ready to deploy?** Just upload `bookkeeping.html` to your server or follow the GitHub Pages instructions above!
