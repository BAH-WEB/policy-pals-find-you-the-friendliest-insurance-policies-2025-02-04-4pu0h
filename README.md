# PolicyPals Landing Page - Maintenance Guide

This guide will help you maintain and customize the PolicyPals landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To modify:

1. Company Name:
```html
<a href="#" class="text-2xl font-bold text-blue-500">PolicyPals</a>
```
- Replace "PolicyPals" with your desired company name
- Adjust text size using `text-2xl` (options: text-lg, text-xl, text-3xl)

2. Navigation Menu Items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-blue-400 transition-colors duration-300">Features</a>
    <!-- Other menu items -->
</div>
```
- Update text between `<a>` tags
- Keep the `href` attributes matching section IDs

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Policy Pals Find You The Friendliest Insurance Policies
</h1>
```
- Update headline text between the `<h1>` tags
- Maintain responsive text sizes:
  - `text-4xl`: Mobile devices
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-800 rounded-xl p-8">
    <div class="text-blue-500 mb-6">
        <i class="fas fa-fingerprint text-4xl"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Personalised Policy Matching</h3>
    <p class="text-gray-400">Advanced algorithms match you...</p>
</div>
```
To modify:
1. Change icon: Update `fa-fingerprint` to any [Font Awesome](https://fontawesome.com/icons) icon
2. Update heading: Modify text in `<h3>` tags
3. Update description: Change text in `<p>` tags

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Internal links (same page):
   - Keep the `#` prefix
   - Match the ID of the target section
   - Example: `href="#features"` links to `<section id="features">`

2. External links:
```html
<a href="https://www.PolicyPals.Co.Uk" class="bg-blue-600">
    Get Started
</a>
```
- Replace URL with your desired destination
- Always include `https://` or `http://`

### Call-to-Action (CTA) Buttons
Located in hero and CTA sections:
```html
<a href="https://www.PolicyPals.Co.Uk" class="inline-block bg-blue-600">
    Find Your Perfect Policy
</a>
```
- Update `href` attribute with your conversion page URL
- Modify button text between `<a>` tags

## Adding Privacy and Terms Pages

### Footer Links Setup
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-blue-400">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-blue-400">Terms of Service</a></li>
</ul>
```

To link to new pages:
1. Create new files:
   - `privacy.html`
   - `terms.html`

2. Update links in footer:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400">Terms of Service</a></li>
```

3. Maintain consistent styling:
   - Copy the header and footer from index.html
   - Use matching Tailwind classes for consistency

## Troubleshooting

### Common Issues

1. Broken Internal Links
- Check that section IDs match href attributes exactly
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. Responsive Design Issues
- Always maintain the responsive class patterns:
  ```html
  class="text-base md:text-lg lg:text-xl"
  ```
- Don't remove `md:` or `lg:` prefixes

3. Missing Icons
- Verify Font Awesome inclusion in header
- Check icon names on Font Awesome website
- Use correct prefix (fas, far, fab)

### Getting Help
- Check [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Join Tailwind CSS community on Discord

Remember to test all changes across different screen sizes using browser developer tools (F12 key).