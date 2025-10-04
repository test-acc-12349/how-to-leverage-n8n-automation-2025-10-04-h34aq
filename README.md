# n8n Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the n8n landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Text Content Updates

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    How to leverage n8n automation
</h1>
```
To update the main headline:
1. Locate the `<h1>` tag in the hero section
2. Replace the text between the opening and closing tags
3. Maintain the existing classes to preserve styling

#### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Fast API</h3>
    <p class="text-gray-600">Integrate with any API quickly and efficiently...</p>
</div>
```
To update feature content:
1. Find the feature card you want to modify
2. Update the `<h3>` title text
3. Modify the description in the `<p>` tag

### Tailwind CSS Classes Explained

#### Common Class Patterns
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-4` (margin bottom)
- Colors: `text-blue-600` (text color), `bg-white` (background color)
- Responsive Design: `md:text-2xl` (applies at medium screens and up)
- Hover Effects: `hover:bg-blue-700` (background color on hover)

#### Modifying Responsive Classes
Example of responsive text:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
- `text-4xl`: Default size on mobile
- `md:text-5xl`: Size on medium screens (768px+)
- `lg:text-6xl`: Size on large screens (1024px+)

## Managing Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="https://n8n.com">Get Started</a>
</div>
```

To update links:
1. Locate the `<a>` tag you want to modify
2. Update the `href` attribute:
   - For internal sections, use `#section-id`
   - For external links, use the full URL
3. Update the link text between the tags

### Footer Links
Footer link structure:
```html
<ul class="space-y-2">
    <li><a href="#features">Features</a></li>
    <li><a href="#benefits">Benefits</a></li>
    <li><a href="https://n8n.com">Get Started</a></li>
</ul>
```

To update footer links:
1. Find the appropriate `<ul>` section
2. Modify the `href` attribute in the `<a>` tag
3. Update the link text
4. Maintain the existing classes for consistent styling

## Adding Privacy and Terms Pages

### Updating Footer Legal Links
Current placeholder structure:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in `href` attributes
   - Verify file names match exactly
   - Ensure files are in the correct directory

2. **Responsive Design Issues**
   - Test at different screen sizes using browser dev tools
   - Verify media query classes (md:, lg:) are correctly formatted
   - Check for missing responsive classes

3. **Styling Inconsistencies**
   - Compare classes with working elements
   - Ensure all Tailwind classes are spelled correctly
   - Check for conflicting classes

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify the Tailwind CDN is loading properly
3. Compare your changes against the original code
4. Test the page in multiple browsers

Remember to always backup your code before making changes and test thoroughly after each modification.