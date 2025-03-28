# HVAC Santa Clara Landing Page - Maintenance Guide

This guide will help you maintain and customize the HVAC Santa Clara landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name**: Locate this code in the header:
```html
<a href="/" class="text-2xl font-bold text-blue-600">HVAC<span class="text-gray-800">Santa Clara</span></a>
```
- Change "HVAC" and "Santa Clara" to your desired text
- Keep the `<span>` tag to maintain the two-tone color effect

2. **Navigation Menu Items**: Find these lines:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="px-6 py-2 bg-blue-600 text-white rounded-full hover:bg-blue-700 transition-all duration-300 transform hover:scale-105">Contact Us</a>
</div>
```
- Change text between `>` and `</a>` for each menu item
- Keep the classes intact to maintain styling

### Hero Section
Update the main headline and subtext:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight text-gray-900 mb-6">
    Santa Clara's Trusted HVAC Experts
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">
    Comfort Perfected in Every Santa Clara Home and Business
</p>
```
- Replace text while keeping the heading tags (`<h1>`, `<p>`)
- Don't remove the Tailwind classes as they control:
  - `text-4xl/5xl/6xl`: Text size at different screen sizes
  - `font-bold`: Text weight
  - `mb-6/8`: Bottom margin spacing

### Understanding Tailwind Classes

Common classes used throughout:
- Size classes: `text-sm`, `text-xl`, `text-2xl`, etc.
- Colors: `text-blue-600`, `bg-white`, `text-gray-800`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom)
- Responsive: `md:text-4xl` (applies at medium screens and up)

## Managing Links

### Updating Navigation Links
Current navigation links are:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact Us</a>
```

To update:
1. Change the `href` value to your desired destination
2. For internal page sections, keep the `#` prefix
3. For external links, use complete URLs: `https://example.com`

### Contact Information
Update email links in these locations:
```html
<!-- CTA Section -->
<a href="mailto:info@hvacsantaclara.com">Get in Touch</a>

<!-- Footer -->
<a href="mailto:info@hvacsantaclara.com" class="text-blue-400 hover:text-blue-300">info@hvacsantaclara.com</a>
```
- Replace `info@hvacsantaclara.com` with your email address
- Update both the `href` and visible text

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Locate the footer section and add these links:
```html
<div class="border-t border-gray-800 mt-12 pt-8 text-sm text-gray-400">
    <p>&copy; 2024 HVAC Santa Clara. All rights reserved.</p>
    <!-- Add these lines -->
    <div class="mt-4">
        <a href="/privacy.html" class="text-gray-400 hover:text-blue-400 mr-4">Privacy Policy</a>
        <a href="/terms.html" class="text-gray-400 hover:text-blue-400">Terms of Service</a>
    </div>
</div>
```

### Step 2: Create Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Use this basic template for each:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - HVAC Santa Clara</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="font-sans antialiased text-gray-800 bg-white">
    <!-- Copy header from index.html -->
    
    <main class="container mx-auto px-6 py-32">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Layout**
   - Check that all Tailwind classes remain intact
   - Verify closing tags match opening tags
   - Maintain the responsive classes (e.g., `md:`, `lg:` prefixes)

2. **Links Not Working**
   - Ensure `href` attributes start with `/` for root-relative paths
   - Use `#` for same-page section links
   - Include `https://` for external links

3. **Images Not Loading**
   - Verify image paths are correct
   - Check image URLs are accessible
   - Ensure proper permissions on image files

Remember to:
- Test all changes on multiple screen sizes
- Keep backup copies of working files
- Validate HTML changes in a testing environment first
- Maintain consistent styling across all pages