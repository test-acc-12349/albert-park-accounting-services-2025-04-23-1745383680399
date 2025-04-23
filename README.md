# Albert Park Landing Page - Maintenance Guide

This guide will help you maintain and customize the Albert Park Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To modify:

1. **Company Name**
```html
<!-- Located in header, look for: -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Albert Park
</a>
```
Simply replace "Albert Park" with your desired company name.

### Hero Section
The main headline and subheading are in the hero section:

```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Your financial success is our bottom line
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Expert accounting solutions tailored to your business needs
</p>
```

Key Tailwind classes explained:
- `text-4xl`: Large text on mobile
- `md:text-6xl`: Larger text on medium screens
- `lg:text-7xl`: Largest text on large screens
- `mb-8`: Margin bottom spacing
- `text-gray-300`: Light gray text color

### Features Section
To modify feature cards:

1. Find the `features` section with three cards
2. Each card follows this structure:
```html
<div class="bg-gray-800 rounded-2xl p-8 hover:scale-105 transition-transform duration-300 shadow-xl">
    <!-- Icon container -->
    <div class="w-16 h-16 bg-gradient-to-br from-purple-500 to-pink-500 rounded-xl mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Tax Optimization</h3>
    <p class="text-gray-400">Strategic tax planning and optimization...</p>
</div>
```

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace with your new link
3. Update the text between `<a>` tags

### Call-to-Action Buttons
There are multiple CTA buttons using this template:
```html
<a href="https://theaccountants.com" class="inline-block px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">
    Get Started
</a>
```

Replace `https://theaccountants.com` with your desired URL.

## Adding Privacy and Terms Pages

### Step 1: Create New Files
1. Create two new files in your project folder:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<ul class="space-y-3">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

Update the links:
```html
<ul class="space-y-3">
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure all `href="#section-id"` matches the corresponding section's `id` attribute
   - Check for typos in IDs
   - Verify file paths are correct for privacy and terms pages

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from Tailwind classes
   - Keep the `container` class on parent elements
   - Maintain the responsive grid structure in features section

3. **Gradient Text Not Showing**
   - Ensure these classes stay together:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all script and CSS links are working:
  ```html
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
  ```

Remember to test all changes across different screen sizes using your browser's developer tools before deploying to production.