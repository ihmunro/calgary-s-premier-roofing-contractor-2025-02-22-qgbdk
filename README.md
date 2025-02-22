# Premier Roofing Landing Page - Maintenance Guide

This guide will help you maintain and customize the Premier Roofing landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your company name and navigation menu:

```html
<a href="/" class="text-2xl font-bold text-gray-800">Premier Roofing</a>
```

To update the company name:
1. Locate this line in the header section
2. Replace "Premier Roofing" with your desired text
3. Keep the surrounding HTML tags intact

#### Navigation Menu Classes
The navigation menu uses these key Tailwind classes:
- `space-x-8`: Creates spacing between menu items
- `text-gray-600`: Sets default text color
- `hover:text-gray-900`: Changes text color on hover

Example of modifying menu spacing:
```html
<!-- Increase spacing between menu items -->
<div class="hidden md:flex space-x-12">  <!-- Changed from space-x-8 -->
```

### Hero Section
The main banner section contains:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8 leading-tight">
    Calgary's Premier Roofing Contractor
</h1>
```

To update:
1. Replace the heading text while keeping the classes
2. Adjust text size using these classes:
   - `text-4xl`: Base size
   - `md:text-5xl`: Medium screens
   - `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <!-- Icon container -->
    <div class="w-16 h-16 bg-blue-100 rounded-full">...</div>
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-600">Feature description</p>
</div>
```

To modify:
1. Update the title text in the `<h3>` tag
2. Change the description in the `<p>` tag
3. Adjust colors by modifying:
   - `bg-blue-100` for icon background
   - `text-blue-600` for icon color

## Fixing Broken Links

### Current Link Structure
The page contains these link types:

1. Navigation Menu Links:
```html
<a href="#services" class="text-gray-600 hover:text-gray-900">Services</a>
<a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
<a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
<a href="#contact" class="text-gray-600 hover:text-gray-900">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://calgaryspremierroofer.com" class="inline-block bg-blue-600...">
    Get Your Free Quote
</a>
```

3. Email Links:
```html
<a href="mailto:iainhmunro@gmail.com">Contact Us Now</a>
```

To update links:
1. For internal section links:
   - Ensure the `href` matches the section's `id` attribute
   - Example: `href="#features"` links to `<section id="features">`

2. For external links:
   - Replace the full URL in the `href` attribute
   - Example: `href="https://yournewwebsite.com"`

3. For email links:
   - Update the email address after `mailto:`
   - Example: `href="mailto:your.email@example.com"`

## Linking Privacy and Terms Pages

### Current Footer Structure
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To add proper privacy and terms links:

1. Create your policy pages:
```html
<!-- privacy.html -->
<!DOCTYPE html>
<html>
    <!-- Copy header and footer from index.html -->
    <!-- Add privacy policy content -->
</html>
```

2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. Broken Internal Links
   - Check that section `id` attributes match link `href` values
   - Ensure IDs are unique across the page
   - Example: `<section id="features">` matches `href="#features"`

2. Responsive Design Issues
   - Verify media query classes are correct:
     - `md:` for medium screens
     - `lg:` for large screens
   - Example: `class="text-4xl md:text-5xl lg:text-6xl"`

3. Styling Inconsistencies
   - Keep color classes consistent:
     - Text colors: `text-gray-600`, `text-gray-900`
     - Background colors: `bg-white`, `bg-blue-600`
   - Maintain spacing patterns:
     - Padding: `p-8`, `py-24`, `px-6`
     - Margins: `mb-4`, `mt-12`

Remember to test all changes across different screen sizes and browsers before publishing updates.