# BestBargainsmart Landing Page Maintenance Guide

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
The main site title and navigation items are located in the header. To update:

```html
<!-- Find this section at the top of the page -->
<a href="/" class="text-1xl font-bold text-white">

BestBargainsmart  <!-- Replace this text -->
</a>
```

#### Hero Section
To update the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Discover Surprising Deals  <!-- Replace main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Your One-Stop Shop for Smart Savings  <!-- Replace subheading -->
</p>
```

### Tailwind CSS Classes Explained

#### Common Classes Used:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[number]`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `px-[number]`: Adds horizontal padding (e.g., `px-6`)
- `py-[number]`: Adds vertical padding (e.g., `py-4`)

#### Responsive Design Classes:
```html
<!-- Example of responsive classes -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
- `text-4xl`: Default size for mobile
- `md:text-5xl`: Size for medium screens (768px+)
- `lg:text-6xl`: Size for large screens (1024px+)

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Replace `#features` with your features page URL
2. Replace `#benefits` with your benefits page URL
3. Replace `#contact` with your contact page URL

### Main Call-to-Action Links
Update the shop now buttons:

```html
<!-- Find this button in multiple locations -->
<a href="https://bestbargainsmart.com" class="bg-blue-600 hover:bg-blue-700">
    Shop Now
</a>
```

Replace `https://bestbargainsmart.com` with your actual shop URL.

## Linking Privacy and Terms Pages

### Footer Link Updates
Locate the Legal section in the footer:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-blue-400">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-blue-400">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Replace the `#` in the Privacy Policy link with `/privacy.html`
2. Replace the `#` in the Terms of Service link with `/terms.html`

Example:
```html
<li><a href="/privacy.html" class="text-gray-400 hover:text-blue-400">Privacy Policy</a></li>
<li><a href="/terms.html" class="text-gray-400 hover:text-blue-400">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in URLs
   - Ensure files exist in the correct directory
   - Verify that links start with `/` for root-relative paths

2. **Responsive Design Issues**
   - If mobile layout looks wrong, check for missing `md:` or `lg:` prefixes
   - Verify that the viewport meta tag is present in the head section

3. **Social Media Icons Not Showing**
   - Ensure Font Awesome CSS is properly loaded
   - Check for correct icon class names (e.g., `fab fa-facebook`)

### Style Consistency Tips

- Always maintain the same color scheme using existing classes:
  - Primary blue: `blue-600`
  - Hover blue: `blue-700`
  - Text gray: `gray-300`
  - Background: `gray-900`

- Keep consistent spacing:
  - Section padding: `py-24 px-6`
  - Component margins: `mb-8`, `mb-12`

Remember to test all changes across different screen sizes using your browser's developer tools (F12).

For additional help or questions, contact your development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).
