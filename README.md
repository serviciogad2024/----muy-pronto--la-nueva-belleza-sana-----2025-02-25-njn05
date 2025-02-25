# Landing Page Maintenance Guide

This guide will help you maintain and customize the Belleza Sana landing page. It's written for beginners and provides step-by-step instructions for common modifications.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text**: Find this line and modify the text "Belleza Sana":
```html
<a href="#" class="text-2xl font-bold text-emerald-600">Belleza Sana</a>
```

2. **Navigation Links**: Locate the navigation div:
```html
<div class="hidden md:flex space-x-8">
    <a href="#caracteristicas" class="text-gray-600 hover:text-emerald-600">Características</a>
    <!-- Other navigation items -->
</div>
```

### Hero Section
To update the main headline and subtitle:

1. **Main Headline**: Find and modify:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-gradient-to-r from-emerald-600 to-teal-600 bg-clip-text text-transparent">
    Muy Pronto: La Nueva Belleza Sana 🌿
</h1>
```

2. **Subtitle**: Update this paragraph:
```html
<p class="text-xl md:text-2xl text-gray-600 mb-12 max-w-3xl mx-auto">
    Belleza Natural y Bienestar, Redefiniendo tu Cuidado 🌿
</p>
```

### Understanding Tailwind Classes
Common classes used in this landing page:

- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `md:text-{size}`: Applies text size at medium screens and up
- `bg-{color}-{shade}`: Sets background color
- `text-{color}-{shade}`: Sets text color
- `p-{number}`: Sets padding
- `m-{number}`: Sets margin
- `rounded-{size}`: Controls border radius

Example of modifying a button:
```html
<!-- Original -->
<a href="#" class="inline-block bg-emerald-600 text-white px-8 py-4 rounded-full">

<!-- Modified with larger padding and different color -->
<a href="#" class="inline-block bg-teal-600 text-white px-10 py-5 rounded-full">
```

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:

```html
<a href="#caracteristicas">Características</a>
<a href="#beneficios">Beneficios</a>
<a href="#faq">FAQ</a>
<a href="#contacto">Contacto</a>
```

To update:
1. Replace `#` with your actual URL for external links
2. Ensure section IDs match the href values for internal links
3. Example:
```html
<!-- External link -->
<a href="https://your-site.com/features">Características</a>

<!-- Internal link -->
<a href="#caracteristicas">Características</a>
```

### Call-to-Action Links
Update the main CTA buttons:
```html
<!-- Find this line -->
<a href="https://bellezasana.website" class="inline-block bg-emerald-600...">

<!-- Replace with your actual URL -->
<a href="https://your-actual-website.com" class="inline-block bg-emerald-600...">
```

## Linking Privacy and Terms Pages

### Footer Links Setup
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Política de Privacidad</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Términos de Uso</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Política de Privacidad</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Términos de Uso</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match exactly (including case)
   - Check for extra spaces in href attributes
   - Verify that sections exist in the HTML

2. **Responsive Design Issues**
   - Check that you're using responsive classes (md:, lg:, etc.)
   - Test on different screen sizes
   - Don't remove the viewport meta tag

3. **Style Changes Not Working**
   - Verify Tailwind CSS is properly loaded
   - Check class spelling and format
   - Ensure classes are in the correct order

Remember to:
- Always backup your code before making changes
- Test all links after updating
- View changes on multiple devices and browsers
- Keep the responsive design intact when modifying classes

Need more help? Contact your web developer or visit [Tailwind CSS documentation](https://tailwindcss.com/docs).