# Painters Port Melbourne Landing Page - Maintenance Guide

This guide will help you maintain and customize the Painters Port Melbourne landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**
```html
<!-- Find this line in the header -->
<h1 class="text-2xl font-bold text-blue-600">Painters Port Melbourne</h1>
```
Simply replace "Painters Port Melbourne" with your desired text.

2. **Navigation Menu Items**
```html
<a href="#services" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Services</a>
```
- Change the text between `<a>` tags to update menu items
- The `text-gray-600` class controls text color
- `hover:text-blue-600` changes color on mouse hover

### Hero Section
Located right below the header:
```html
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Quality Interior & Exterior Painting & Decorating Services
</h2>
```
- `text-4xl` sets mobile text size
- `md:text-5xl` sets tablet text size
- `lg:text-6xl` sets desktop text size

### Tailwind CSS Tips
- Font sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-blue-600`, `bg-white`, `text-gray-900`
- Spacing: `p-8` (padding), `m-4` (margin), `mb-6` (margin-bottom)
- Responsive prefixes: `md:` (tablet), `lg:` (desktop)

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
To update:
1. The `#` symbol indicates an internal page section
2. Ensure the href matches the section's ID attribute
3. Example: `href="#services"` links to `<section id="services">`

### Contact Links
Phone and email links:
```html
<a href="tel:0466344447">Call 0466 344 447</a>
<a href="mailto:quote@paintersportmelbourne.com.au">Email Us</a>
```
To update:
1. Replace phone number in both `href="tel:..."` and displayed text
2. Update email in `href="mailto:..."` attribute

### Common Link Issues
- Missing `#` for internal links
- Incorrect section IDs
- Wrong email/phone format in href attributes

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the footer's Quick Links section:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in the same folder as `index.html`
2. Copy the header and footer from `index.html` to maintain consistent styling
3. Add your policy content between the header and footer

### Step 3: Style Consistency
Use these classes for policy page headings:
```html
<h1 class="text-3xl font-bold text-center mb-16">Privacy Policy</h1>
```

For content paragraphs:
```html
<p class="text-gray-600 mb-4">Your policy content here</p>
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Internal Links**
   - Check that section IDs match href attributes exactly
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Always include responsive classes (`md:`, `lg:`)
   - Test on different screen sizes
   - Example: `class="text-xl md:text-2xl lg:text-3xl"`

3. **Style Inconsistencies**
   - Copy existing classes for similar elements
   - Keep color codes consistent (e.g., `blue-600`)
   - Maintain consistent spacing patterns

4. **Contact Link Problems**
   - Use `tel:` for phone numbers
   - Use `mailto:` for email addresses
   - Remove spaces from phone numbers in href attributes

Need more help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).