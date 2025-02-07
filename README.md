# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this section -->
<div class="text-2xl font-bold text-gray-800">
    Texas Web Design  <!-- Change this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
The main headline and call-to-action area:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8 leading-tight">
    Best Websites In Texas  <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Premium web design solutions  <!-- Update subheading -->
</p>
```

#### Understanding Tailwind Classes
Common classes used throughout:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-4`, `mb-8`)
- `px-[size]`: Adds horizontal padding
- `py-[size]`: Adds vertical padding
- `bg-[color]`: Sets background color

Example of modifying a button:
```html
<!-- Original button -->
<a href="https://twd.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">

<!-- To make button larger with different color -->
<a href="https://twd.com" class="inline-block bg-green-600 text-white px-10 py-5 rounded-lg">
```

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<!-- Hero section -->
<a href="https://twd.com">Get Started Today</a>

<!-- CTA section -->
<a href="https://twd.com">Contact Us Now</a>
```

### Updating Links
To update any link:
1. Locate the `<a>` tag
2. Change the `href` attribute value
3. For internal links (same page sections), use `#section-id`
4. For external links, use full URL including `https://`

Example:
```html
<!-- Change this -->
<a href="https://twd.com">

<!-- To this -->
<a href="https://your-actual-domain.com">
```

## Linking Privacy and Terms Pages

### Footer Link Updates
Locate the legal section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <!-- Update these href attributes -->
        <li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Adding New Policy Pages
1. Create new files named `privacy.html` and `terms.html` in the same directory
2. Ensure consistent styling by copying the header and footer from `index.html`
3. Add your policy content between the header and footer

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Verify that section IDs match the href attributes
   - Example: `href="#features"` needs matching `id="features"` in section tag

2. **Responsive Design Issues**
   - Check for proper responsive classes (md:, lg:)
   - Example: `text-xl md:text-2xl lg:text-3xl`

3. **Missing Icons**
   - Verify Font Awesome is loaded properly
   - Check icon class names match exactly: `fas fa-server`

### Need Help?
- Double-check all closing tags
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Inspect element using browser developer tools (F12)
- Compare changes against original code

Remember to always backup your files before making changes, and test all updates in a development environment first.