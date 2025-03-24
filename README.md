# Landing Page Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections Overview
The landing page is divided into these key sections:
- Header (TWD logo and navigation)
- Hero Section (main banner)
- Features Section
- Benefits Section
- FAQ Section
- CTA (Call to Action) Section
- Footer

### Updating Text Content

#### Hero Section
To update the main headline and subheading:
```html
<!-- Find these lines in the Hero Section -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">Best Websites In Texas</p>
```
Simply replace the text between the tags while keeping the tags intact.

#### Features Cards
To modify feature descriptions:
```html
<!-- Located in the Features Section -->
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Custom Design</h3>
    <p class="text-gray-600 leading-relaxed">Unique, professional designs tailored to your brand and business needs.</p>
</div>
```
Update the text within the `<h3>` and `<p>` tags for each feature card.

### Understanding Tailwind CSS Classes

#### Common Class Patterns
- Text sizes: `text-xl`, `text-2xl`, `text-4xl`
- Colors: `text-gray-600`, `text-blue-600`
- Spacing: `mb-4` (margin bottom), `p-8` (padding)
- Responsive design: `md:text-5xl` (applies at medium screens)

#### Example: Modifying Button Styles
```html
<!-- Original button -->
<a href="htttps://twd.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg text-lg font-semibold hover:bg-blue-700 transform hover:scale-105 transition-all duration-300 shadow-lg">Get Started Today</a>

<!-- To change color to red -->
<a href="htttps://twd.com" class="inline-block bg-red-600 text-white px-8 py-4 rounded-lg text-lg font-semibold hover:bg-red-700 transform hover:scale-105 transition-all duration-300 shadow-lg">Get Started Today</a>
```

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the text between the tags

### External Links
The following external links need attention:
```html
<!-- Main CTA button -->
<a href="htttps://twd.com">Get Started Today</a>

<!-- Footer email -->
<a href="mailto:admin@twd.com">admin@twd.com</a>

<!-- Social media links -->
<a href="#"><i class="fab fa-twitter"></i></a>
<a href="#"><i class="fab fa-facebook"></i></a>
<a href="#"><i class="fab fa-linkedin"></i></a>
```

Replace the `#` or placeholder URLs with actual social media profiles.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs and href values
   - Verify that section IDs are unique

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag in the header
   - Test on different screen sizes

3. **Icon Problems**
   - Verify Font Awesome CDN link is working
   - Check icon class names against Font Awesome documentation
   - Ensure internet connectivity for CDN access

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all CDN links are accessible
3. Test the page in multiple browsers
4. Ensure all HTML tags are properly closed

Remember to always backup your files before making changes, and test your updates in a development environment first.