# Landing Page Maintenance Guide
## For Computerbril.org

This guide provides detailed instructions for maintaining and customizing the Computerbril.org landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-gray-800">Computerbril.org</a>
```
Simply replace "Computerbril.org" with your desired text.

### Hero Section
The main banner section contains your primary heading and call-to-action buttons:

1. **Main Heading:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Computerbril Aftrekbaar ZZP 2025
</h1>
```
- Replace the text between the `<h1>` tags
- Keep the classes intact to maintain responsive sizing:
  - `text-4xl`: Mobile size
  - `md:text-5xl`: Tablet size
  - `lg:text-6xl`: Desktop size

2. **Subheading:**
```html
<p class="text-xl md:text-2xl text-gray-600 mb-8">
    Tijdelijk 20% Korting - Profiteer Nu van Fiscaal Voordeel
</p>
```
- Update the text between the `<p>` tags
- Maintain the existing classes for consistent styling

### Benefits Section
To modify the benefits cards:

```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Fiscaal Voordeel 2025</h3>
    <p class="text-gray-600">Profiteer nu van maximale belastingaftrek...</p>
</div>
```
- Each benefit card is wrapped in this structure
- Update the `<h3>` title and `<p>` description
- Keep the surrounding `div` and classes for proper styling

## Managing Links

### Navigation Menu Links
The main navigation is located in the header:

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#voordelen" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Voordelen</a>
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="https://computerbril.org/winkel" class="bg-blue-600 text-white px-6 py-2 rounded-full hover:bg-blue-700">Bestel Nu</a>
</div>
```

To update links:
1. Internal page sections: Use `#section-name`
2. External pages: Use full URL starting with `https://`
3. Always test links after updating

### Call-to-Action Buttons
Update the main CTA buttons in the hero section:

```html
<a href="https://computerbril.org/winkel" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full">
    Bestel Met Korting
</a>
```
- Replace the `href` value with your shop URL
- Keep the classes to maintain button styling

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the footer's legal section:

```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Juridisch</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Layout:**
   - Check that you haven't removed any important Tailwind classes
   - Verify all opening tags have matching closing tags
   - Ensure proper nesting of elements

2. **Links Not Working:**
   - Confirm file paths are correct
   - Check for typos in URLs
   - Verify files exist in the specified location

3. **Responsive Issues:**
   - Keep all responsive classes (starting with `sm:`, `md:`, `lg:`)
   - Test on different screen sizes
   - Don't remove the viewport meta tag in the header

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Keep a backup copy of the original file before making changes

Remember to always test your changes across different devices and browsers to ensure everything works as expected.