# Landing Page Maintenance Guide

This guide will help you maintain and customize the Nachtbril Action landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Logo Text:**
```html
<div class="text-2xl font-bold text-blue-600">Nachtbril Action</div>
```
- Simply replace "Nachtbril Action" with your desired text
- The `text-2xl` makes it larger, `text-blue-600` makes it blue

2. **Navigation Links:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-700 hover:text-blue-600">Voordelen</a>
    <!-- More links... -->
</div>
```
- Replace text between `<a>` tags with your desired link names
- Keep the `href` attributes matching your section IDs

### Hero Section
The main banner section contains:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900 mb-8 leading-tight">
    Nachtbril Action<br>
    <span class="text-blue-600">Tijdelijk 20% KORTING!</span>
</h1>
```
- First line: Main heading
- Second line: Blue highlighted text
- `text-4xl`, `md:text-5xl`, `lg:text-6xl` control text size on different screen sizes

### Tailwind CSS Quick Reference
Common classes used in this page:
- `container mx-auto`: Centers content and sets max-width
- `px-6`: Adds horizontal padding
- `py-24`: Adds vertical padding
- `text-gray-600`: Sets text color
- `bg-white`: Sets background color
- `rounded-xl`: Rounds corners
- `shadow-lg`: Adds shadow effect

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Voordelen</a>
<a href="#benefits">Kenmerken</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Identify the section ID you want to link to
2. Add a `#` before the section ID in the `href`
3. Example: `<a href="#new-section">New Section</a>`

### Call-to-Action Links
Current external link:
```html
<a href="https://nachtbril.com/shop" class="inline-block bg-blue-600 text-white">
```
To update:
1. Replace the URL in `href` with your shop/action URL
2. Test the link before deploying
3. Consider adding `target="_blank"` for external links

## Adding Privacy and Terms Pages

### Footer Modification
Add these links to your footer section:

```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <!-- Existing footer content -->
    <div>
        <h3 class="text-lg font-semibold mb-4">Legal</h3>
        <ul class="space-y-2">
            <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
            <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Creating Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Use the same header and footer as `index.html`
3. Add your policy content in the main section
4. Maintain consistent styling using Tailwind classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify media query classes (md:, lg:) are correct
   - Example: `hidden md:flex` hides on mobile, shows on medium screens

3. **Styling Problems**
   - Confirm Tailwind CSS is loading properly
   - Check for typos in class names
   - Use browser inspector to verify applied styles

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check browser console for errors
- Verify all CDN links are accessible

Remember to always test changes in multiple browsers and screen sizes before deploying to production.