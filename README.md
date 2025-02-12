# Priority Limousine Landing Page - Maintenance Guide

This guide will help you maintain and customize the Priority Limousine landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**
```html
<!-- Find this line in the header section -->
<h1 class="text-2xl font-bold text-gray-900">Priority Limo</h1>
```
- Simply replace "Priority Limo" with your desired text
- The `text-2xl` class controls size (options: text-sm, text-lg, text-2xl, text-3xl)

### Hero Section
Located at the top of the page with the main headline:

```html
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Your preferred priority choice
</h2>
```
- Replace "Your preferred priority choice" with your headline
- The different text sizes (`text-4xl`, `md:text-5xl`, `lg:text-6xl`) ensure proper scaling on different devices
- Don't remove these classes unless you understand responsive design

### Features Cards
Each feature card follows this structure:
```html
<div class="p-8 bg-white rounded-xl shadow-lg hover:shadow-xl transition duration-300">
    <i class="fas fa-crown text-4xl text-gray-900 mb-6"></i>
    <h4 class="text-xl font-semibold mb-4">Luxury</h4>
    <p class="text-gray-600">Immerse yourself in the epitome of automotive luxury</p>
</div>
```
To modify:
1. Change icon: Replace `fa-crown` with any [Font Awesome icon](https://fontawesome.com/icons)
2. Update heading: Replace "Luxury" text
3. Update description: Modify the paragraph text
4. Keep the class structure intact for consistent styling

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<nav class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-700 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-700 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-700 hover:text-gray-900 transition-colors duration-300">Contact</a>
</nav>
```

To update:
1. Internal links (same page): Keep the `#` format (e.g., `#features`)
2. External links: Replace with full URL (e.g., `https://example.com/page`)
3. Don't remove the classes as they control hover effects and spacing

### Booking Links
Find and update all booking links:
```html
<!-- In Hero Section -->
<a href="bookinglink.com" class="inline-flex items-center px-8 py-4 bg-gray-900 text-white">
<!-- In CTA Section -->
<a href="bookinglink.com" class="inline-flex items-center px-8 py-4 bg-white text-gray-900">
```
Replace `bookinglink.com` with your actual booking system URL

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate these lines in the footer:
```html
<li><a href="#" class="text-gray-600 hover:text-gray-900">Privacy Policy</a></li>
<li><a href="#" class="text-gray-600 hover:text-gray-900">Terms of Service</a></li>
```

Replace with:
```html
<li><a href="privacy.html" class="text-gray-600 hover:text-gray-900">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-600 hover:text-gray-900">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Styling**
   - If styles disappear, check that the Tailwind CSS CDN link is present:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

2. **Missing Icons**
   - If icons don't show, verify the Font Awesome link:
   ```html
   <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
   ```

3. **Links Not Working**
   - For internal links (#features, #benefits, etc.), ensure the ID exists in the corresponding section
   - Example: `<section id="features">` matches `href="#features"`

### Need Help?
- Double-check all closing tags
- Verify all links start with `http://` or `https://` for external URLs
- Keep the responsive classes (`md:`, `lg:`) to maintain mobile compatibility
- Test the page on different devices after making changes

Remember to always backup your files before making significant changes!