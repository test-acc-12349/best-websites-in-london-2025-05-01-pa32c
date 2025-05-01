# London Web Landing Page - Maintenance Guide

This guide will help you maintain and customize the London Web landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Company Name/Logo**
```html
<!-- Located in header, around line 20 -->
<div class="text-2xl font-bold text-gray-800">
    <a href="/" class="flex items-center space-x-2">
        <span>London Web</span> <!-- Change this text -->
    </a>
</div>
```

2. **Navigation Menu Items**
```html
<!-- Located in header, around line 25 -->
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <!-- Update text between <a> tags to change menu items -->
</div>
```

### Hero Section
To modify the main headline and subheading:

```html
<!-- Located after header, around line 53 -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Best Websites In London <!-- Change this text -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Custom Websites For Your Business <!-- Change this text -->
</p>
```

### Tailwind CSS Class Guide
Common classes used and their purposes:

- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-semibold`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-6`, `mb-10`)
- `py-[size]`: Adds padding top and bottom (e.g., `py-24`)
- `bg-[color]`: Sets background color (e.g., `bg-white`, `bg-blue-600`)

To modify styling, replace the number in the class name:
```html
<!-- Example: Change padding from 24 to 32 -->
<section class="py-24"> <!-- Change to py-32 -->
```

## Managing Links

### Navigation Links
Current navigation links are:

```html
<!-- Located in header -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Locate the link you want to change
2. Modify the `href` attribute
3. Update both desktop and mobile menu versions

Example:
```html
<!-- Change Features link to About -->
<a href="#about" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">About</a>
```

### Call-to-Action Buttons
Current CTA buttons link to "https://sigmaseo.io". To update:

```html
<!-- Located in header and hero section -->
<a href="https://sigmaseo.io" class="font-medium">Get Started</a>
```

Replace the URL with your desired destination:
```html
<a href="https://your-website.com" class="font-medium">Get Started</a>
```

## Adding Privacy and Terms Pages

### 1. Create New Pages
Create two new files in your project:
- `privacy.html`
- `terms.html`

### 2. Update Footer Links
Locate the footer section and update the placeholder links:

```html
<!-- Located in footer, around line 170 -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### 3. Maintain Consistent Styling
When creating privacy.html and terms.html, copy these classes from the footer:
- Link styling: `class="text-gray-400 hover:text-white transition-colors duration-300"`
- Heading styling: `class="text-lg font-semibold mb-4"`

## Troubleshooting

Common issues and solutions:

1. **Broken Links**
   - Check if file paths are correct
   - Ensure files exist in the specified location
   - Verify that href attributes start with "/" for root-relative paths

2. **Styling Issues**
   - Make sure Tailwind CSS is properly loaded
   - Check for typos in class names
   - Verify that responsive classes (md:, lg:) are in the correct order

3. **Mobile Menu Problems**
   - Verify Alpine.js is properly loaded
   - Check that x-data and x-show attributes are present
   - Ensure mobile menu HTML structure matches desktop

For additional help:
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check the [Alpine.js documentation](https://alpinejs.dev/docs)
- Validate your HTML using [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different devices and browsers before deploying to production.