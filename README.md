# Magic City Yachts Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Magic City Yachts landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page consists of these key sections:
- Header/Navigation (fixed at top)
- Hero Section (first view with main heading)
- Features Section
- Benefits Section
- FAQ Section
- Contact Section
- Footer

### Updating Text Content

#### Header and Navigation
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-['Playfair_Display'] font-bold text-blue-900">Magic City Yachts</a>
```
To change the company name:
1. Locate this line in the header section
2. Replace "Magic City Yachts" with your desired text
3. Keep the surrounding HTML tags and classes intact

#### Hero Section Text
```html
<h1 class="font-['Playfair_Display'] text-4xl md:text-5xl lg:text-6xl font-bold text-blue-900 leading-tight mb-6">
    Luxury Yacht Rentals in Miami for Unforgettable Ocean Escapes
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 font-light">
    Sail Miami in Style. Unforgettable Views.
</p>
```
To modify the main headline and subheading:
1. Find these elements in the hero section
2. Update the text between the opening and closing tags
3. Maintain the existing HTML structure

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
The landing page uses Tailwind's responsive prefixes:
- `md:` - applies styles at medium screens (768px and up)
- `lg:` - applies styles at large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Default size: text-4xl (36px)
- Medium screens: text-5xl (48px)
- Large screens: text-6xl (60px)

#### Common Tailwind Classes Used
- Text Colors: `text-blue-900`, `text-gray-600`, `text-white`
- Background Colors: `bg-white`, `bg-blue-900`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-6` (margin bottom)
- Flex Layout: `flex`, `items-center`, `justify-between`

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Book Now</a>
</div>
```

To update internal links:
1. Locate the `href` attribute
2. Ensure the # matches the `id` of the target section
3. Example: `href="#features"` links to `<section id="features">`

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-white/80 hover:text-white transition-colors duration-300">
        <!-- Facebook icon -->
    </a>
</div>
```

To update social media links:
1. Replace the `#` with your actual social media URL
2. Example: `href="https://facebook.com/magiccityyachts"`
3. Repeat for Twitter and Instagram links

## Adding Privacy and Terms Pages

### Adding Footer Links
Add these links to the footer's Quick Links section:
```html
<ul class="space-y-4">
    <!-- Existing links -->
    <li><a href="privacy.html" class="text-white/80 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-white/80 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Creating New Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Responsive Design Issues**
   - Test at different screen sizes
   - Ensure responsive classes (md:, lg:) are properly ordered
   - Use browser developer tools to inspect elements

3. **Missing Styles**
   - Verify Tailwind CDN link is present in the head section
   - Check for typos in class names
   - Ensure classes are space-separated

### Need Help?
For additional assistance:
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using Chrome DevTools

Remember to always test changes across different devices and browsers before pushing to production.