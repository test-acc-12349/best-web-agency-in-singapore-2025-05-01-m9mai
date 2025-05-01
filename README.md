# WebAgencySG Landing Page Maintenance Guide

This guide will help you maintain and customize the WebAgencySG landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name:**
```html
<!-- Located in the header section -->
<div class="text-xl font-bold tracking-tight">
    <a href="/" class="text-white hover:text-blue-400 transition duration-300">
        WebAgency<span class="text-blue-500">SG</span>
    </a>
</div>
```
- Replace `WebAgency` and `SG` with your brand name
- The blue highlight is controlled by `text-blue-500`

### Hero Section
The main banner section includes:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Best Web Agency In Singapore
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    Grow your business with clicks
</p>
```
- Update the heading and subheading text as needed
- Text sizes use responsive classes:
  - `text-4xl`: Default size
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-900 rounded-xl p-8">
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-400">Intuitive interface designed for...</p>
</div>
```
To modify:
1. Change the heading text in `<h3>`
2. Update the description in `<p>`
3. Maintain the existing classes for consistent styling

### Tailwind CSS Tips for Beginners
- Colors use format: `text-{color}-{shade}` (e.g., `text-blue-500`)
- Spacing uses format: `m-{size}` for margin, `p-{size}` for padding
- Responsive prefixes: `md:` (medium), `lg:` (large)
- Don't remove `transition` or `duration` classes as they control animations

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition duration-300">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition duration-300">FAQ</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition duration-300">Contact</a>
</div>
```
To update:
1. Locate the `href` attribute
2. For internal sections, use `#section-name`
3. For external links, use full URL: `https://example.com`
4. Update both desktop and mobile menu sections

### Call-to-Action Links
Currently points to:
```html
<a href="https://fixrr.online" class="inline-block bg-blue-600...">
```
Replace `https://fixrr.online` with your desired URL

### Footer Links
Update these placeholder links:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition duration-300">About</a></li>
    <li><a href="#" class="hover:text-white transition duration-300">Services</a></li>
    <li><a href="#" class="hover:text-white transition duration-300">Blog</a></li>
</ul>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links:
```html
<!-- Before -->
<li><a href="#" class="hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="#" class="hover:text-white transition duration-300">Terms of Service</a></li>

<!-- After -->
<li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="hover:text-white transition duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in `href` attributes
   - Ensure file names match exactly
   - Verify file locations in your directory

2. **Styling Issues**
   - Don't remove `class` attributes
   - Keep responsive classes (`md:`, `lg:`)
   - Maintain the spacing classes

3. **Mobile Menu Problems**
   - Keep Alpine.js script tag in header
   - Don't modify `x-data` attributes
   - Ensure mobile menu items match desktop navigation

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Alpine.js Documentation](https://alpinejs.dev/)

Remember to test all changes across different screen sizes using your browser's developer tools.