# RecipesPinned Landing Page - Maintenance Guide

This guide will help you maintain and customize the RecipesPinned landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-indigo-600">RecipesPinned</a>
```
- Replace "RecipesPinned" with your brand name
- Adjust text size using Tailwind classes:
  - `text-xl` (smaller)
  - `text-2xl` (current size)
  - `text-3xl` (larger)

### Hero Section
The main banner section with background image:

1. **Update Main Heading**
```html
<h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6">
    Why Do 10,000+ Cooks Save These Recipe Ideas Daily? Find Out!
</h1>
```
- Edit text between the `<h1>` tags
- Keep the classes intact for responsive design
  - `text-4xl`: size on mobile
  - `md:text-6xl`: size on desktop

2. **Background Image**
```html
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" 
     alt="Cooking background" 
     class="w-full h-full object-cover">
```
- Replace the `src` URL with your image
- Update the `alt` text for accessibility

### Features Section
To modify feature cards:

1. **Icon Updates**
```html
<i class='bx bx-star text-4xl'></i>
```
- Change icons by replacing `bx-star` with other [Boxicons](https://boxicons.com/) names
- Available icons: `bx-dish`, `bx-chef`, etc.

2. **Feature Text**
```html
<h3 class="text-xl font-bold mb-4">Most-Saved & Free!</h3>
<p class="text-gray-600">Access the most popular and trending recipes that everyone loves.</p>
```
- Update heading and description text
- Maintain the existing classes for consistent styling

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Benefits</a>
</div>
```
To update:
1. Change `href="#features"` to link to different sections
2. Use `#section-id` for internal links
3. Use full URLs for external links (e.g., `href="https://example.com"`)

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <i class='bx bxl-pinterest text-2xl'></i>
    </a>
</div>
```
Replace `href="#"` with your social media profiles:
- Pinterest: `href="https://pinterest.com/your-profile"`
- Instagram: `href="https://instagram.com/your-profile"`
- Facebook: `href="https://facebook.com/your-page"`

## Adding Policy Pages

### Step 1: Create Policy Pages
Create two new files in your project:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```
- Replace `href="#"` with proper file paths
- Keep the existing classes for consistent hover effects

## Troubleshooting

### Common Issues

1. **Broken Images**
If images don't appear:
- Check image URL in `src` attribute
- Ensure image files exist in correct location
- Verify file permissions

2. **Responsive Design Issues**
If layout breaks on mobile:
- Don't remove `md:` prefixed classes
- Keep the `container` class on parent elements
- Maintain the responsive grid classes (`grid-cols-1 md:grid-cols-2`)

3. **Icon Problems**
If icons don't show:
- Verify Boxicons CSS link in header is working
- Check icon class names match Boxicons documentation
- Ensure internet connection for CDN access

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML syntax at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always backup your files before making changes, and test on multiple devices and browsers after updates.