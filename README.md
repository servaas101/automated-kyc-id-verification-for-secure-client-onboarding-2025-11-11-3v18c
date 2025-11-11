# Somda Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize the Somda KYC & ID Verification landing page. Whether you're updating text, fixing links, or adding new content, this guide breaks everything down into simple, manageable steps.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Updating Text and Content](#updating-text-and-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing Broken Links](#fixing-broken-links)
5. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
6. [Troubleshooting](#troubleshooting)
7. [Best Practices](#best-practices)

---

## Getting Started

### What You Need to Know

Before making changes to this landing page, understand these basics:

- **HTML** is the structure (the skeleton of the page)
- **CSS** is the styling (how things look - colors, sizes, spacing)
- **Tailwind CSS** is a utility-based framework that uses pre-made CSS classes
- **Links (href)** are the connections between pages

### Tools You'll Need

- A text editor (VS Code, Sublime Text, or even Notepad)
- A web browser to preview changes
- Basic understanding of finding and replacing text

### File Structure

Your landing page consists of:

```
project-folder/
├── index.html          (Main landing page - what you're customizing)
├── privacy.html        (Privacy policy page - needs to be created)
├── terms.html          (Terms of service page - needs to be created)
└── blog.html           (Blog page - already referenced)
```

---

## Updating Text and Content

### Understanding the Page Sections

Your landing page has these main sections:

1. **Header/Navigation** - Top menu bar
2. **Hero Section** - Large welcome area with main headline
3. **Features Section** - Three feature cards
4. **Benefits Section** - Six benefit cards
5. **Testimonials Section** - Client quotes
6. **FAQ Section** - Questions and answers
7. **Contact Section** - Contact form
8. **Footer** - Bottom information

### How to Update Text

**Step 1: Open Your HTML File**

Open `index.html` in your text editor. You should see the code starting with `<!DOCTYPE html>`.

**Step 2: Find the Text You Want to Change**

Use your text editor's "Find" function:
- **Windows/Linux**: Press `Ctrl + F`
- **Mac**: Press `Cmd + F`

A search box will appear.

**Step 3: Locate and Replace**

Type the text you want to find and replace it.

### Specific Examples

#### Updating the Hero Section Title

**Location**: Lines 108-112

**Current Code**:
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-white mb-6 leading-tight">
    Automated <span class="section-title">KYC & ID Verification</span> for Secure Client Onboarding
</h1>
```

**How to Change It**:

1. Open `index.html` in your text editor
2. Press `Ctrl + F` (or `Cmd + F` on Mac)
3. Search for: `Automated KYC & ID Verification`
4. Replace with your new text

**Example - New Text**:
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-white mb-6 leading-tight">
    Fast & Secure <span class="section-title">Identity Verification</span> Solutions
</h1>
```

**Important**: Keep the `<span class="section-title">` tags around the highlighted text to maintain the purple color.

---

#### Updating the Hero Subtitle

**Location**: Lines 114-117

**Current Code**:
```html
<p class="text-xl md:text-2xl text-gray-300 mb-8 max-w-3xl mx-auto leading-relaxed font-light">
    Verify clients in seconds — Stay fully compliant with regulatory requirements while providing a seamless onboarding experience
</p>
```

**How to Change It**:

1. Search for: `Verify clients in seconds`
2. Replace the entire text between the `<p>` and `</p>` tags

**Example - New Text**:
```html
<p class="text-xl md:text-2xl text-gray-300 mb-8 max-w-3xl mx-auto leading-relaxed font-light">
    Complete identity verification in under 5 seconds with 99.9% accuracy
</p>
```

---

#### Updating Feature Cards

**Location**: Lines 169-239 (Features Section)

**Current Code Example** (First Feature Card):
```html
<div class="feature-card">
    <div class="mb-6 inline-flex items-center justify-center w-16 h-16 rounded-full gradient-primary">
        <i data-lucide="zap" class="w-8 h-8 text-white"></i>
    </div>
    <h3 class="text-2xl font-bold text-white mb-4">Real-time KYC Checks</h3>
    <p class="text-gray-300 font-light leading-relaxed mb-4">
        Instant verification against global databases, sanctions lists, and regulatory watchlists...
    </p>
```

**How to Change Feature Title**:

1. Search for: `Real-time KYC Checks`
2. Replace with your new title

**How to Change Feature Description**:

1. Search for the description text starting with: `Instant verification against global databases...`
2. Replace the entire paragraph

**How to Change Feature Icon**:

The `<i data-lucide="zap"` part controls the icon. Available icons include:
- `zap` (lightning bolt)
- `face` (face)
- `shield-alert` (shield)
- `rocket` (rocket)
- `lock` (lock)
- `shield-check` (checkmark shield)
- `trending-down` (downward trend)
- `link` (link)
- `headphones` (headphones)

**Example - Change Icon**:
```html
<!-- Old -->
<i data-lucide="zap" class="w-8 h-8 text-white"></i>

<!-- New -->
<i data-lucide="rocket" class="w-8 h-8 text-white"></i>
```

---

#### Updating Benefit Cards

**Location**: Lines 281-378 (Benefits Section)

**Current Code Example**:
```html
<div class="feature-card">
    <div class="mb-6 inline-flex items-center justify-center w-16 h-16 rounded-full bg-gradient-to-r from-orange-500 to-red-500">
        <i data-lucide="rocket" class="w-8 h-8 text-white"></i>
    </div>
    <h3 class="text-2xl font-bold text-white mb-3">Faster Onboarding</h3>
    <p class="text-gray-300 font-light leading-relaxed">
        Reduce your average onboarding time from hours to minutes...
    </p>
    <div class="mt-4 text-accent-text font-semibold">
        Average time saved: 85%
    </div>
</div>
```

**How to Change Benefit Title**:

1. Search for: `Faster Onboarding`
2. Replace with your new title

**How to Change Benefit Description**:

1. Search for the description text
2. Replace the entire paragraph

**How to Change the Metric/Statistic**:

1. Search for: `Average time saved: 85%`
2. Replace with your new statistic

---

#### Updating Testimonials

**Location**: Lines 487-556 (Testimonials Section)

**Current Code Example** (First Testimonial):
```html
<div class="testimonial-card">
    <div class="flex items-center gap-1 mb-4">
        <i data-lucide="star" class="w-5 h-5 star fill-current"></i>
        <i data-lucide="star" class="w-5 h-5 star fill-current"></i>
        <i data-lucide="star" class="w-5 h-5 star fill-current"></i>
        <i data-lucide="star" class="w-5 h-5 star fill-current"></i>
        <i data-lucide="star" class="w-5 h-5 star fill-current"></i>
    </div>
    <p class="text-gray-300 font-light leading-relaxed mb-6">
        "Somda's KYC solution has been a game-changer..."
    </p>
    <div>
        <p class="font-bold text-white">Sarah Chen</p>
        <p class="text-gray-400 text-sm font-light">Head of Compliance, FinFlow Technologies</p>
    </div>
</div>
```

**How to Change the Testimonial Quote**:

1. Search for: `"Somda's KYC solution has been a game-changer..."`
2. Replace with your new testimonial (keep the quotation marks)

**How to Change the Client Name**:

1. Search for: `Sarah Chen`
2. Replace with the new name

**How to Change the Client Title**:

1. Search for: `Head of Compliance, FinFlow Technologies`
2. Replace with the new title and company

**How to Change the Star Rating**:

To change from 5 stars to fewer stars, delete star lines. For example, to show 4 stars:

```html
<!-- Remove one of these lines -->
<i data-lucide="star" class="w-5 h-5 star fill-current"></i>
```

---

#### Updating FAQ Questions and Answers

**Location**: Lines 650-785 (FAQ Section)

**Current Code Example**:
```html
<div class="faq-item">
    <div class="faq-question feature-card cursor-pointer flex items-center justify-between">
        <h3 class="text-lg font-bold text-white">How long does the verification process take?</h3>
        <i data-lucide="chevron-down" class="faq-icon w-6 h-6 text-gray-400"></i>
    </div>
    <div class="faq-answer hidden mt-4 px-6 py-4 bg-gray-800 rounded-lg">
        <p class="text-gray-300 font-light leading-relaxed">
            Our verification process typically completes in less than 5 seconds...
        </p>
    </div>
</div>
```

**How to Change the FAQ Question**:

1. Search for: `How long does the verification process take?`
2. Replace with your new question

**How to Change the FAQ Answer**:

1. Search for the answer text starting with: `Our verification process typically completes...`
2. Replace the entire paragraph

**How to Add Bullet Points in FAQ Answers**:

Replace a simple paragraph with a list:

```html
<!-- Old -->
<p class="text-gray-300 font-light leading-relaxed">
    Your answer text here.
</p>

<!-- New -->
<ul class="space-y-2 text-gray-300 font-light">
    <li class="flex items-start gap-3">
        <i data-lucide="check" class="w-5 h-5 accent-text flex-shrink-0 mt-0.5"></i>
        <span>First bullet point</span>
    </li>
    <li class="flex items-start gap-3">
        <i data-lucide="check" class="w-5 h-5 accent-text flex-shrink-0 mt-0.5"></i>
        <span>Second bullet point</span>
    </li>
</ul>
```

---

#### Updating Hero Statistics

**Location**: Lines 127-141

**Current Code**:
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-2xl mx-auto mt-16">
    <div class="text-center">
        <div class="text-4xl font-bold accent-text mb-2">99.9%</div>
        <p class="text-gray-400 font-light">Accuracy Rate</p>
    </div>
    <div class="text-center">
        <div class="text-4xl font-bold accent-text mb-2">&lt;5s</div>
        <p class="text-gray-400 font-light">Verification Time</p>
    </div>
    <div class="text-center">
        <div class="text-4xl font-bold accent-text mb-2">180+</div>
        <p class="text-gray-400 font-light">Countries Supported</p>
    </div>
</div>
```

**How to Change the First Statistic**:

1. Search for: `99.9%`
2. Replace with your new number
3. Search for: `Accuracy Rate`
4. Replace with your new label

**How to Change All Statistics**:

Repeat the process for each statistic (the middle and last ones).

---

#### Updating Footer Contact Information

**Location**: Lines 1035-1070 (Contact Info in Footer)

**Current Code**:
```html
<div class="flex items-start gap-4">
    <i data-lucide="mail" class="w-6 h-6 text-accent-text flex-shrink-0 mt-1"></i>
    <div>
        <p class="text-gray-400 font-light text-sm">Email</p>
        <a href="mailto:info@somda.co.za" class="text-white hover:text-accent-text transition-colors duration-300">info@somda.co.za</a>
    </div>
</div>
```

**How to Change Email Address**:

1. Search for: `info@somda.co.za`
2. Replace with your email address (appears twice - in the link and the display text)

**How to Change Website URL**:

1. Search for: `www.somda.co.za`
2. Replace with your website URL

---

### Summary: Text Update Locations

| Content | Search For | Location |
|---------|-----------|----------|
| Main Title | "Automated KYC & ID Verification" | Hero Section |
| Subtitle | "Verify clients in seconds" | Hero Section |
| Feature Titles | "Real-time KYC Checks" | Features Section |
| Benefit Titles | "Faster Onboarding" | Benefits Section |
| Testimonial Quotes | "Somda's KYC solution..." | Testimonials Section |
| FAQ Questions | "How long does..." | FAQ Section |
| Email | "info@somda.co.za" | Footer |
| Website | "www.somda.co.za" | Footer |

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind CSS

Tailwind CSS uses simple class names to style elements. Instead of writing custom CSS, you add classes to HTML elements.

**Example**:
```html
<!-- This creates a button with padding, background color, and text color -->
<button class="px-6 py-3 bg-blue-600 text-white rounded-lg">
    Click Me
</button>
```

### Common Tailwind Classes in Your Landing Page

#### Text Size Classes

| Class | Size | Used For |
|-------|------|----------|
| `text-sm` | Small | Captions, small text |
| `text-base` | Normal | Body text |
| `text-lg` | Large | Subheadings |
| `text-2xl` | Extra Large | Section titles |
| `text-4xl` | Huge | Statistics |
| `text-5xl` | Massive | Main titles |

#### Text Color Classes

| Class | Color | Used For |
|-------|-------|----------|
| `text-white` | White | Main text |
| `text-gray-300` | Light Gray | Secondary text |
| `text-gray-400` | Medium Gray | Tertiary text |
| `text-gray-950` | Dark Gray/Black | Backgrounds |
| `accent-text` | Green/Teal | Highlights |
| `section-title` | Purple | Section highlights |

#### Spacing Classes

| Class | Effect |
|-------|--------|
| `mb-4` | Margin bottom (space below) |
| `mb-6` | Larger margin bottom |
| `mt-4` | Margin top (space above) |
| `px-4` | Padding horizontal (left & right) |
| `py-3` | Padding vertical (top & bottom) |
| `gap-4` | Space between items |

#### Display/Layout Classes

| Class | Effect |
|-------|--------|
| `flex` | Makes items line up horizontally |
| `grid` | Creates a grid layout |
| `grid-cols-1` | 1 column on mobile |
| `md:grid-cols-2` | 2 columns on medium screens |
| `lg:grid-cols-3` | 3 columns on large screens |
| `hidden` | Hides element |
| `md:hidden` | Hides on medium+ screens |

#### Background Classes

| Class | Effect |
|-------|--------|
| `bg-gray-950` | Dark background |
| `bg-gray-900` | Slightly lighter background |
| `bg-blue-600` | Blue background |
| `gradient-primary` | Purple gradient |
| `gradient-accent` | Green/teal gradient |

### Practical Examples

#### Change Button Colors

**Current Button Code** (Line 119):
```html
<a href="https://somda.co.za/contact" class="btn-primary text-lg">
    Start Verification Now
</a>
```

The `btn-primary` class is defined in the `<style>` section (lines 22-32). To change the color:

**Option 1: Change the Style Definition**

Find this in the `<style>` section (line 24):
```css
.btn-primary {
    background-color: #5B4BFF;  /* This is purple */
    color: white;
    transition: all 0.3s ease-in-out;
    border-radius: 50px;
    padding: 12px 32px;
    font-weight: 600;
}
```

Change `#5B4BFF` to a new color code:
- `#3B82F6` for blue
- `#10B981` for green
- `#F59E0B` for orange
- `#EF4444` for red

**Option 2: Use Tailwind Classes Directly**

Replace `class="btn-primary text-lg"` with:
```html
class="bg-blue-600 hover:bg-blue-700 text-white rounded-full px-8 py-3 font-semibold transition-all duration-300 text-lg"
```

---

#### Change Section Background Colors

**Current Code** (Line 143):
```html
<section id="features" class="py-24 bg-gray-900 relative overflow-hidden">
```

To change the background:

Replace `bg-gray-900` with:
- `bg-gray-950` for darker
- `bg-blue-900` for blue tint
- `bg-purple-900` for purple tint

**Example**:
```html
<section id="features" class="py-24 bg-blue-900 relative overflow-hidden">
```

---

#### Change Card Styling

**Current Feature Card Code** (Lines 186-189):
```html
<div class="feature-card">
    <div class="mb-6 inline-flex items-center justify-center w-16 h-16 rounded-full gradient-primary">
        <i data-lucide="zap" class="w-8 h-8 text-white"></i>
    </div>
```

To change the icon background color, modify `gradient-primary`:

Replace `gradient-primary` with:
- `bg-gradient-to-r from-blue-500 to-cyan-500` for blue gradient
- `bg-gradient-to-r from-green-500 to-emerald-500` for green gradient
- `bg-red-600` for solid red

**Example**:
```html
<div class="mb-6 inline-flex items-center justify-center w-16 h-16 rounded-full bg-gradient-to-r from-blue-500 to-cyan-500">
    <i data-lucide="zap" class="w-8 h-8 text-white"></i>
</div>
```

---

#### Change Text Size

**Current Title Code** (Line 109):
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-white mb-6 leading-tight">
```

The classes mean:
- `text-5xl` = size on mobile
- `md:text-6xl` = size on medium screens
- `lg:text-7xl` = size on large screens

To make it smaller:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-6 leading-tight">
```

To make it larger:
```html
<h1 class="text-6xl md:text-7xl lg:text-8xl font-bold text-white mb-6 leading-tight">
```

---

#### Change Responsive Layout

**Current Grid Code** (Line 176):
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
```

This means:
- `grid-cols-1` = 1 column on mobile
- `md:grid-cols-3` = 3 columns on medium screens
- `gap-8` = spacing between items

To change to 2 columns on medium screens:
```html
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
```

To change to 4 columns on large screens:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
```

---

#### Change Spacing

**Current Code** (Line 114):
```html
<p class="text-xl md:text-2xl text-gray-300 mb-8 max-w-3xl mx-auto leading-relaxed font-light">
```

The `mb-8` means "margin bottom 8 units". To change spacing:

- `mb-2` = very small space below
- `mb-4` = small space below
- `mb-6` = medium space below
- `mb-8` = large space below
- `mb-12` = very large space below

**Example - Reduce spacing**:
```html
<p class="text-xl md:text-2xl text-gray-300 mb-4 max-w-3xl mx-auto leading-relaxed font-light">
```

---

### Responsive Design Breakpoints

Tailwind uses these prefixes for different screen sizes:

| Prefix | Screen Size | When Used |
|--------|-------------|----------|
| (none) | Mobile | Default - applies to all sizes |
| `sm:` | Small (640px+) | Tablets |
| `md:` | Medium (768px+) | Larger tablets |
| `lg:` | Large (1024px+) | Desktops |
| `xl:` | Extra Large (1280px+) | Large desktops |

**Example**:
```html
<!-- Mobile: 1 column, Tablets: 2 columns, Desktop: 3 columns -->
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3">
```

---

### Common Customizations

#### Make Mobile Menu Visible by Default

**Current Code** (Line 99):
```html
<div class="mobile-menu hidden absolute top-16 left-0 right-0 bg-gray-900 border-b border-gray-800 md:hidden">
```

The `hidden` class hides it. To show it:
```html
<div class="mobile-menu absolute top-16 left-0 right-0 bg-gray-900 border-b border-gray-800 md:hidden">
```

---

#### Change Hero Section Height

**Current Code** (Line 104):
```html
<section class="relative min-h-screen flex items-center justify-center overflow-hidden bg-gradient-to-b from-gray-950 via-gray-900 to-gray-950">
```

`min-h-screen` means "minimum height of full screen". To change:

- `min-h-96` = shorter hero
- `min-h-screen` = full screen (default)
- `min-h-[600px]` = custom height (600 pixels)

**Example - Shorter hero**:
```html
<section class="relative min-h-96 flex items-center justify-center overflow-hidden bg-gradient-to-b from-gray-950 via-gray-900 to-gray-950">
```

---

#### Change Border Radius (Rounded Corners)

**Current Code** (Line 187):
```html
<div class="mb-6 inline-flex items-center justify-center w-16 h-16 rounded-full gradient-primary">
```

`rounded-full` = completely round. Options:
- `rounded-none` = no rounding
- `rounded-sm` = slightly rounded
- `rounded-md` = medium rounding
- `rounded-lg` = rounded
- `rounded-full` = completely round

**Example - Less rounded**:
```html
<div class="mb-6 inline-flex items-center justify-center w-16 h-16 rounded-lg gradient-primary">
```

---

### Summary: Common Customizations

| What to Change | Current | New Option |
|---|---|---|
| Button color | `btn-primary` | `bg-blue-600` |
| Section background | `bg-gray-900` | `bg-blue-900` |
| Text size | `text-5xl` | `text-4xl` or `text-6xl` |
| Text color | `text-white` | `text-gray-300` |
| Spacing | `mb-8` | `mb-4` or `mb-12` |
| Grid columns | `md:grid-cols-3` | `md:grid-cols-2` |
| Border radius | `rounded-full` | `rounded-lg` |

---

## Fixing Broken Links

### Understanding Links

A link in HTML looks like this:

```html
<a href="https://example.com">Click Here</a>
```

- `<a>` = anchor tag (creates a link)
- `href="..."` = the destination address
- `Click Here` = the text you see

### Types of Links

**External Links** (go to other websites):
```html
<a href="https://somda.co.za/contact">Contact Us</a>
```

**Internal Links** (go to other pages on your site):
```html
<a href="privacy.html">Privacy Policy</a>
```

**Anchor Links** (jump to sections on same page):
```html
<a href="#features">Go to Features</a>
```

---

### Finding All Links in Your Landing Page

**Navigation Links** (Line 85-92):
```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
<a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
<a href="#testimonials" class="text-gray-300 hover:text-white transition-colors duration-300">Testimonials</a>
```

**CTA Buttons** (Line 119-124):
```html
<a href="https://somda.co.za/contact" class="btn-primary text-lg">
    Start Verification Now
</a>
<button class="btn-secondary text-lg">
    Watch Demo
</button>
```

**Footer Links** (Lines 1000-1020):
```html
<a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a>
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
```

---

### Step-by-Step: Fix Broken Links

#### Step 1: Identify Broken Links

Open your landing page in a web browser and click each link. If it doesn't work or shows a 404 error, it's broken.

**Common Broken Links in Your Page**:

1. **"Get Started" buttons** - Point to `https://somda.co.za/contact`
2. **"Watch Demo" button** - No link assigned
3. **"Schedule Demo" button** - Points to `https://somda.co.za/contact`
4. **Footer links** - Point to `privacy.html`, `terms.html`, `blog.html` (may not exist)

---

#### Step 2: Fix Contact/CTA Links

**Location**: Multiple places throughout the page

**Current Code** (Example from Line 119):
```html
<a href="https://somda.co.za/contact" class="btn-primary text-lg">
    Start Verification Now
</a>
```

**How to Fix**:

1. Replace `https://somda.co.za/contact` with your actual contact page URL
2. Examples of valid URLs:
   - `https://yourcompany.com/contact`
   - `https://yourcompany.com/contact-us`
   - `contact.html` (if on same server)
   - `#contact` (to jump to contact section on page)

**Updated Example**:
```html
<a href="https://yourcompany.com/contact" class="btn-primary text-lg">
    Start Verification Now
</a>
```

---

#### Step 3: Fix the "Watch Demo" Button

**Location**: Line 123

**Current Code**:
```html
<button class="btn-secondary text-lg">
    Watch Demo
</button>
```

This is a button, not a link. To make it functional:

**Option A: Link to Your Demo Page**
```html
<a href="https://yourcompany.com/demo" class="btn-secondary text-lg">
    Watch Demo
</a>
```

**Option B: Link to a Video**
```html
<a href="https://youtube.com/watch?v=YOUR_VIDEO_ID" class="btn-secondary text-lg" target="_blank">
    Watch Demo
</a>
```

**Option C: Link to a Demo Video on Your Server**
```html
<a href="demo.html" class="btn-secondary text-lg">
    Watch Demo
</a>
```

---

#### Step 4: Fix Navigation Links

**Location**: Lines 85-92 (Desktop Menu) and Lines 95-101 (Mobile Menu)

**Current Code**:
```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
<a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
<a href="#testimonials" class="text-gray-300 hover:text-white transition-colors duration-300">Testimonials</a>
```

These links use `#` to jump to sections. Verify the section IDs exist:

**Check 1**: Search for `id="features"` - Should find it at Line 143
**Check 2**: Search for `id="benefits"` - Should find it at Line 248
**Check 3**: Search for `id="faq"` - Should find it at Line 600
**Check 4**: Search for `id="testimonials"` - Should find it at Line 420

If any are missing, add them to the corresponding section:

```html
<!-- Example: Add id to Features section if missing -->
<section id="features" class="py-24 bg-gray-900 relative overflow-hidden">
```

---

#### Step 5: Fix Footer Links

**Location**: Lines 1000-1020 (Footer Product Column)

**Current Code**:
```html
<li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
<li><a href="#benefits" class="text-gray-400 hover:text-white transition-colors duration-300">Benefits</a></li>
<li><a href="#faq" class="text-gray-400 hover:text-white transition-colors duration-300">FAQ</a></li>
<li><a href="https://somda.co.za/contact" class="text-gray-400 hover:text-white transition-colors duration-300">Pricing</a></li>
```

**How to Fix**:

1. The anchor links (`#features`, `#benefits`, `#faq`) should work if sections exist
2. Replace `https://somda.co.za/contact` with your pricing page URL

**Updated Example**:
```html
<li><a href="https://yourcompany.com/pricing" class="text-gray-400 hover:text-white transition-colors duration-300">Pricing</a></li>
```

---

#### Step 6: Fix Footer Company Links

**Location**: Lines 1021-1026 (Footer Company Column)

**Current Code**:
```html
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">About Us</a></li>
<li><a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
<li><a href="https://somda.co.za/contact" class="text-gray-400 hover:text-white transition-colors duration-300">Contact</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Careers</a></li>
```

**Issues**:
- `href="#"` doesn't work (goes nowhere)
- `href="blog.html"` needs to exist or be updated

**How to Fix**:

1. Replace `#` with actual page URLs:
```html
<li><a href="about.html" class="text-gray-400 hover:text-white transition-colors duration-300">About Us</a></li>
```

2. Update `blog.html` to your actual blog page:
```html
<li><a href="https://yourcompany.com/blog" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
```

3. Update contact link:
```html
<li><a href="https://yourcompany.com/contact" class="text-gray-400 hover:text-white transition-colors duration-300">Contact</a></li>
```

4. Fix careers link:
```html
<li><a href="https://yourcompany.com/careers" class="text-gray-400 hover:text-white transition-colors duration-300">Careers</a></li>
```

---

#### Step 7: Fix Footer Legal Links

**Location**: Lines 1027-1032 (Footer Legal Column)

**Current Code**:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Security</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Compliance</a></li>
```

**Issues**:
- `privacy.html` and `terms.html` may not exist (we'll fix these next)
- `#` links don't work

**How to Fix** (covered in next section):

See "Linking Privacy and Terms Pages" below.

---

#### Step 8: Fix Footer Contact Links

**Location**: Lines 1050-1065 (Footer Contact Info)

**Current Code**:
```html
<a href="mailto:info@somda.co.za" class="text-white hover:text-accent-text transition-colors duration-300">info@somda.co.za</a>
```

**How to Fix**:

Replace `info@somda.co.za` with your actual email address (appears twice):

```html
<a href="mailto:your-email@yourcompany.com" class="text-white hover:text-accent-text transition-colors duration-300">your-email@yourcompany.com</a>
```

---

#### Step 9: Fix Social Media Links

**Location**: Lines 1074-1091 (Footer Social Links)

**Current Code**:
```html
<a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center text-gray-400 hover:text-white hover:bg-accent-text transition-all duration-300">
    <i class="fab fa-twitter"></i>
</a>
```

**How to Fix**:

Replace `#` with your actual social media URLs:

```html
<!-- Twitter -->
<a href="https://twitter.com/yourhandle" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center text-gray-400 hover:text-white hover:bg-accent-text transition-all duration-300" target="_blank">
    <i class="fab fa-twitter"></i>
</a>

<!-- LinkedIn -->
<a href="https://linkedin.com/company/yourcompany" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center text-gray-400 hover:text-white hover:bg-accent-text transition-all duration-300" target="_blank">
    <i class="fab fa-linkedin"></i>
</a>

<!-- GitHub -->
<a href="https://github.com/yourprofile" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center text-gray-400 hover:text-white hover:bg-accent-text transition-all duration-300" target="_blank">
    <i class="fab fa-github"></i>
</a>

<!-- Facebook -->
<a href="https://facebook.com/yourpage" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center text-gray-400 hover:text-white hover:bg-accent-text transition-all duration-300" target="_blank">
    <i class="fab fa-facebook"></i>
</a>
```

**Note**: The `target="_blank"` attribute opens links in a new tab.

---

### Complete Link Reference Table

| Link Type | Current | Location | Fix |
|-----------|---------|----------|-----|
| Start Verification | `https://somda.co.za/contact` | Line 119 | Update to your contact page |
| Watch Demo | `<button>` (no link) | Line 123 | Convert to `<a>` tag with URL |
| Schedule Demo | `https://somda.co.za/contact` | Line 407 | Update to your contact page |
| Features Nav | `#features` | Line 86 | Verify section exists |
| Benefits Nav | `#benefits` | Line 87 | Verify section exists |
| FAQ Nav | `#faq` | Line 88 | Verify section exists |
| Testimonials Nav | `#testimonials` | Line 89 | Verify section exists |
| Privacy Policy | `privacy.html` | Line 1029 | Create file or update URL |
| Terms of Service | `terms.html` | Line 1030 | Create file or update URL |
| Blog | `blog.html` | Line 1024 | Create file or update URL |
| Email | `info@somda.co.za` | Line 1053 | Update to your email |
| Twitter | `#` | Line 1077 | Update to your Twitter URL |
| LinkedIn | `#` | Line 1082 | Update to your LinkedIn URL |
| GitHub | `#` | Line 1087 | Update to your GitHub URL |
| Facebook | `#` | Line 1092 | Update to your Facebook URL |

---

## Linking Privacy and Terms Pages

### What You Need to Do

Your landing page currently references `privacy.html` and `terms.html`, but these files don't exist yet. You need to:

1. Create these files
2. Update the links to point to them
3. Add content to them

---

### Step 1: Create the Privacy Policy Page

**Step 1A: Create a new file**

1. Open your text editor
2. Create a new file
3. Save it as `privacy.html` in the same folder as `index.html`

**Step 1B: Add basic HTML structure**

Copy and paste this template into `privacy.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Somda KYC & ID Verification">
    <meta name="author" content="Somda">
    <title>Privacy Policy | Somda</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Space Grotesk', sans-serif;
            font-weight: 700;
            letter-spacing: -0.02em;
        }
        
        body {
            font-weight: 300;
            background-color: #0f172a;
            color: #e2e8f0;
        }
    </style>
</head>
<body class="bg-gray-950 text-gray-100">
    <!-- Header Navigation (same as index.html) -->
    <header class="sticky top-0 z-50 bg-gray-950 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 rounded-full bg-gradient-to-r from-purple-600 to-purple-500 flex items-center justify-center">
                    <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                    </svg>
                </div>
                <span class="text-xl font-bold text-white" style="font-family: 'Space Grotesk';">SOMDA</span>
            </div>

            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300">Home</a>
            </div>

            <div class="hidden md:block">
                <a href="index.html#contact" class="bg-purple-600 hover:bg-purple-700 text-white rounded-full px-6 py-2 transition-colors duration-300">Back to Home</a>
            </div>
        </nav>
    </header>

    <!-- Privacy Policy Content -->
    <section class="py-24 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-white mb-8">Privacy Policy</h1>
            
            <div class="prose prose-invert max-w-none space-y-8">
                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">1. Introduction</h2>
                    <p class="text-gray-300 font-light leading-relaxed">
                        Somda ("we", "us", "our", or "Company") operates the website and provides KYC and ID verification services. This page informs you of our policies regarding the collection, use, and disclosure of personal data when you use our Service and the choices you have associated with that data.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">2. Information Collection and Use</h2>
                    <p class="text-gray-300 font-light leading-relaxed mb-4">
                        We collect several different types of information for various purposes to provide and improve our Service to you.
                    </p>
                    <h3 class="text-xl font-bold text-white mb-3">Types of Data Collected:</h3>
                    <ul class="list-disc list-inside space-y-2 text-gray-300 font-light">
                        <li>Personal identification information (name, email address, phone number)</li>
                        <li>Government-issued identification documents</li>
                        <li>Biometric data (facial recognition for verification purposes)</li>
                        <li>Address and proof of residence information</li>
                        <li>Usage data and analytics</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">3. Use of Data</h2>
                    <p class="text-gray-300 font-light leading-relaxed mb-4">
                        Somda uses the collected data for various purposes:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-300 font-light">
                        <li>To provide and maintain our Service</li>
                        <li>To verify client identity and comply with regulatory requirements</li>
                        <li>To detect, prevent and address fraud and security issues</li>
                        <li>To provide customer support and respond to inquiries</li>
                        <li>To gather analysis or valuable information so we can improve our Service</li>
                        <li>To monitor the usage of our Service</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">4. Security of Data</h2>
                    <p class="text-gray-300 font-light leading-relaxed">
                        The security of your data is important to us but remember that no method of transmission over the Internet or method of electronic storage is 100% secure. While we strive to use commercially acceptable means to protect your Personal Data, we cannot guarantee its absolute security. We use industry-standard encryption (AES-256) and maintain ISO 27001 certification to protect your information.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">5. Changes to This Privacy Policy</h2>
                    <p class="text-gray-300 font-light leading-relaxed">
                        We may update our Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page and updating the "effective date" at the top of this Privacy Policy.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">6. Contact Us</h2>
                    <p class="text-gray-300 font-light leading-relaxed">
                        If you have any questions about this Privacy Policy, please contact us at:
                    </p>
                    <p class="text-gray-300 font-light mt-4">
                        Email: <a href="mailto:privacy@somda.co.za" class="text-purple-400 hover:text-purple-300">privacy@somda.co.za</a>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 border-t border-gray-800 py-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400 font-light">
                &copy; 2025 Somda. All rights reserved.
            </p>
            <div class="mt-4 flex justify-center gap-6">
                <a href="index.html" class="text-gray-400 hover:text-white transition-colors duration-300">Home</a>
                <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy</a>
                <a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms</a>
            </div>
        </div>
    </footer>
</body>
</html>
```

---

### Step 2: Create the Terms of Service Page

**Step 2A: Create a new file**

1. Open your text editor
2. Create a new file
3. Save it as `terms.html` in the same folder as `index.html`

**Step 2B: Add basic HTML structure**

Copy and paste this template into `terms.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Somda KYC & ID Verification">
    <meta name="author" content="Somda">
    <title>Terms of Service | Somda</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Space Grotesk', sans-serif;
            font-weight: 700;
            letter-spacing: -0.02em;
        }
        
        body {
            font-weight: 300;
            background-color: #0f172a;
            color: #e2e8f0;
        }
    </style>
</head>
<body class="bg-gray-950 text-gray-100">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-gray-950 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 rounded-full bg-gradient-to-r from-purple-600 to-purple-500 flex items-center justify-center">
                    <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                    </svg>
                </div>
                <span class="text-xl font-bold text-white" style="font-family: 'Space Grotesk';">SOMDA</span>
            </div>

            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300">Home</a>
            </div>

            <div class="hidden md:block">
                <a href="index.html#contact" class="bg-purple-600 hover:bg-purple-700 text-white rounded-full px-6 py-2 transition-colors duration-300">Back to Home</a>
            </div>
        </nav>
    </header>

    <!-- Terms of Service Content -->
    <section class="py-24 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-white mb-8">Terms of Service</h1>
            
            <div class="prose prose-invert max-w-none space-y-8">
                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">1. Agreement to Terms</h2>
                    <p class="text-gray-300 font-light leading-relaxed">
                        By accessing and using this website and service, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">2. Use License</h2>
                    <p class="text-gray-300 font-light leading-relaxed mb-4">
                        Permission is granted to temporarily download one copy of the materials (information or software) on Somda's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-300 font-light">
                        <li>Modifying or copying the materials</li>
                        <li>Using the materials for any commercial purpose or for any public display</li>
                        <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                        <li>Removing any copyright or other proprietary notations from the materials</li>
                        <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">3. Disclaimer</h2>
                    <p class="text-gray-300 font-light leading-relaxed">
                        The materials on Somda's website are provided on an 'as is' basis. Somda makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">4. Limitations</h2>
                    <p class="text-gray-300 font-light leading-relaxed">
                        In no event shall Somda or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Somda's website.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">5. Accuracy of Materials</h2>
                    <p class="text-gray-300 font-light leading-relaxed">
                        The materials appearing on Somda's website could include technical, typographical, or photographic errors. Somda does not warrant that any of the materials on its website are accurate, complete, or current. Somda may make changes to the materials contained on its website at any time without notice.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">6. Links</h2>
                    <p class="text-gray-300 font-light leading-relaxed">
                        Somda has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Somda of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">7. Modifications</h2>
                    <p class="text-gray-300 font-light leading-relaxed">
                        Somda may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">8. Governing Law</h2>
                    <p class="text-gray-300 font-light leading-relaxed">
                        These terms and conditions are governed by and construed in accordance with the laws of South Africa, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">9. Contact Information</h2>
                    <p class="text-gray-300 font-light leading-relaxed">
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="text-gray-300 font-light mt-4">
                        Email: <a href="mailto:legal@somda.co.za" class="text-purple-400 hover:text-purple-300">legal@somda.co.za</a>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 border-t border-gray-800 py-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400 font-light">
                &copy; 2025 Somda. All rights reserved.
            </p>
            <div class="mt-4 flex justify-center gap-6">
                <a href="index.html" class="text-gray-400 hover:text-white transition-colors duration-300">Home</a>
                <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy</a>
                <a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms</a>
            </div>
        </div>
    </footer>
</body>
</html>
```

---

### Step 3: Verify Links in index.html

Now that you've created `privacy.html` and `terms.html`, verify that the links in your `index.html` point to them correctly.

**Check Footer Links**:

**Location**: Lines 1029-1032

Current code should be:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

If the links are different, update them to match exactly.

---

### Step 4: Update Links in Footer

**Location**: Lines 1095-1097

Current code:
```html
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
<a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a>
```

These should match your file names. If you don't have a `blog.html` file, either:

**Option A**: Create it (same process as privacy.html)

**Option B**: Link to an external blog:
```html
<a href="https://yourcompany.com/blog" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a>
```

---

### Step 5: Test All Links

1. Open `index.html` in your web browser
2. Click on each link to verify it works:
   - "Privacy Policy" link in footer
   - "Terms of Service" link in footer
   - "Back to Home" link in privacy.html
   - "Back to Home" link in terms.html

---

### Summary: Privacy and Terms Setup

| File | What to Do | Status |
|------|-----------|--------|
| `privacy.html` | Create new file with template provided | ✓ Create |
| `terms.html` | Create new file with template provided | ✓ Create |
| `index.html` Line 1029 | Verify link to `privacy.html` | ✓ Verify |
| `index.html` Line 1030 | Verify link to `terms.html` | ✓ Verify |
| `index.html` Line 1095 | Verify link to `privacy.html` | ✓ Verify |
| `index.html` Line 1096 | Verify link to `terms.html` | ✓ Verify |

---

## Troubleshooting

### Common Issues and Solutions

#### Issue 1: Links Don't Work

**Problem**: You click a link and nothing happens, or you get a 404 error.

**Solutions**:

1. **Check the file path**:
   - If linking to `privacy.html`, make sure the file exists in the same folder as `index.html`
   - Verify the filename spelling is exact (case-sensitive on some servers)

2. **Check the href value**:
   - Make sure it's spelled correctly: `href="privacy.html"` (not `href="privacy.htm"`)
   - Check for extra spaces: `href=" privacy.html"` (wrong)

3. **Test with a simple link**:
   ```html
   <a href="test.html">Test Link</a>
   ```
   Create `test.html` and verify this works before troubleshooting other links.

---

#### Issue 2: Anchor Links Don't Jump to Sections

**Problem**: Clicking "Features" in the menu doesn't jump to the Features section.

**Solutions**:

1. **Verify the section ID exists**:
   ```html
   <!-- This is what you're linking to -->
   <a href="#features">Features</a>

   <!-- This section must have matching ID -->
   <section id="features" class="...">
   ```

2. **Check for typos**:
   - Link says `href="#features"` but section says `id="feature"` (missing 's')
   - Link says `href="#Features"` but section says `id="features"` (case mismatch)

3. **Add missing ID if needed**:
   ```html
   <!-- If section doesn't have ID, add it -->
   <section id="features" class="py-24 bg-gray-900 relative overflow-hidden">
   ```

---

#### Issue 3: Styling Looks Wrong After Changes

**Problem**: After changing Tailwind classes, the page looks broken or ugly.

**Solutions**:

1. **Check for typos in class names**:
   ```html
   <!-- Wrong -->
   <div class="text-5xl">Wrong Size</div>

   <!-- Right -->
   <div class="text-5xl">Right Size</div>
   ```

2. **Don't mix custom CSS with Tailwind**:
   ```html
   <!-- Don't do this -->
   <div class="text-5xl" style="font-size: 30px;">Conflicting</div>

   <!-- Do this instead -->
   <div class="text-5xl">Correct</div>
   ```

3. **Verify responsive classes**:
   ```html
   <!-- Make sure responsive prefixes are correct -->
   <div class="text-base md:text-lg lg:text-2xl">
       Correct responsive sizing
   </div>
   ```

4. **Clear browser cache**:
   - Press `Ctrl + Shift + Delete` (or `Cmd + Shift + Delete` on Mac)
   - Clear cached images and files
   - Reload the page

---

#### Issue 4: Text Doesn't Display Correctly

**Problem**: Text appears cut off, too small, or hard to read.

**Solutions**:

1. **Check text color**:
   ```html
   <!-- If text is white on white background, you can't see it -->
   <div class="bg-white text-white">Invisible</div>

   <!-- Fix: Change text color -->
   <div class="bg-white text-black">Visible</div>
   ```

2. **Check text size**:
   ```html
   <!-- Too small? -->
   <p class="text-xs">Too small</p>

   <!-- Make it bigger -->
   <p class="text-base">Better</p>
   ```

3. **Check line height**:
   ```html
   <!-- Text too cramped? -->
   <p class="leading-none">Cramped</p>

   <!-- Add more space -->
   <p class="leading-relaxed">Better</p>
   ```

---

#### Issue 5: Images or Icons Not Showing

**Problem**: You see broken image icons or missing icons.

**Solutions**:

1. **Check icon names**:
   ```html
   <!-- Wrong icon name -->
   <i data-lucide="zappp">Wrong</i>

   <!-- Correct icon name -->
   <i data-lucide="zap">Correct</i>
   ```

2. **Verify Lucide library is loaded**:
   Check that this line exists in your `<head>` section:
   ```html
   <script src="https://unpkg.com/lucide@latest"></script>
   ```

3. **Initialize Lucide icons**:
   Check that this code exists at the bottom of your `<body>`:
   ```html
   <script>
       lucide.createIcons();
   </script>
   ```

---

#### Issue 6: Mobile Menu Not Working

**Problem**: Mobile menu doesn't open/close on small screens.

**Solutions**:

1. **Check JavaScript is loading**:
   Verify the JavaScript code at the bottom of `index.html` (around line 1140) exists and is not commented out.

2. **Check mobile menu button**:
   ```html
   <!-- Make sure button exists -->
   <button class="mobile-menu-button md:hidden text-white text-2xl">
       <i class="fas fa-bars"></i>
   </button>
   ```

3. **Check mobile menu div**:
   ```html
   <!-- Make sure menu div exists -->
   <div class="mobile-menu hidden absolute ...">
       <!-- Menu items -->
   </div>
   ```

4. **Clear browser cache** and reload.

---

#### Issue 7: Form Not Submitting

**Problem**: Contact form doesn't send messages.

**Solutions**:

1. **Check Web3Forms access key**:
   The form needs a valid access key. If it shows `3bb39263-2490-491b-89f8-213fa513edae`, replace it with your own from web3forms.com.

2. **Verify form fields have correct names**:
   ```html
   <!-- Required fields -->
   <input type="text" name="name" required>
   <input type="email" name="email" required>
   <textarea name="message" required></textarea>
   ```

3. **Check form action URL**:
   ```html
   <!-- Should be -->
   <form action="https://api.web3forms.com/submit" method="POST">
   ```

4. **Test with browser console**:
   - Press `F12` to open developer tools
   - Go to "Console" tab
   - Try submitting the form
   - Look for error messages

---

#### Issue 8: Page Looks Different on Mobile

**Problem**: Layout breaks or looks wrong on phone screens.

**Solutions**:

1. **Check responsive classes**:
   ```html
   <!-- Should have mobile-first approach -->
   <div class="text-base md:text-lg lg:text-2xl">
       Text size adjusts for screen size
   </div>
   ```

2. **Check viewport meta tag**:
   This should exist in `<head>`:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

3. **Test on real phone or use browser DevTools**:
   - Press `F12` in browser
   - Click device icon (top left of DevTools)
   - Select "iPhone" or other device
   - Check if layout looks correct

---

### Quick Troubleshooting Checklist

- [ ] Are all file names spelled correctly?
- [ ] Are all links pointing to the right files?
- [ ] Is the browser cache cleared?
- [ ] Are all HTML tags properly closed?
- [ ] Are all class names spelled correctly?
- [ ] Does the page work in a different browser?
- [ ] Are all required files in the same folder?
- [ ] Is JavaScript enabled in the browser?

---

## Best Practices

### 1. Always Back Up Before Making Changes

**Before you make major changes**:

1. Copy your entire project folder
2. Rename it with a date: `somda-landing-backup-2025-01-15`
3. Keep this backup in case something goes wrong

---

### 2. Make Changes Incrementally

**Don't change everything at once**:

1. Make one change
2. Save the file
3. Refresh the browser
4. Verify it works
5. Then make the next change

This way, if something breaks, you know exactly what caused it.

---

### 3. Use Version Control (Git)

**If you're comfortable with it**:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial landing page"

# Make changes, then commit again
git commit -m "Updated hero text"
```

This lets you revert to previous versions if needed.

---

### 4. Test All Links Regularly

**Create a checklist**:

- [ ] All navigation links work
- [ ] All CTA buttons link to correct pages
- [ ] Footer links work
- [ ] Social media links work
- [ ] Contact form works

**Test on multiple devices**:
- Desktop computer
- Tablet
- Mobile phone
- Different browsers (Chrome, Firefox, Safari)

---

### 5. Keep Content Updated

**Regularly update**:
- Contact information
- Statistics and metrics
- Testimonials
- Feature descriptions
- FAQ items

---

### 6. Use Descriptive Names

**When creating new files or sections**:

```html
<!-- Good: Descriptive -->
<section id="features-overview" class="...">

<!-- Bad: Not descriptive -->
<section id="section1" class="...">
```

---

### 7. Comment Your Changes

**Add comments to document changes**:

```html
<!-- Updated hero title on 2025-01-15 -->
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-white mb-6 leading-tight">
    New Title Here
</h1>
```

---

### 8. Validate Your HTML

**Use a validator**:

1. Go to https://validator.w3.org/
2. Upload your HTML file
3. Fix any errors reported

---

### 9. Optimize Performance

**Keep pages fast**:

- Compress images before adding them
- Use CDN links (like Tailwind and Font Awesome already do)
- Minimize custom CSS
- Remove unused code

---

### 10. Security Best Practices

**Protect your site**:

- Keep software updated
- Use HTTPS (SSL certificate)
- Validate all form inputs
- Never expose sensitive information in HTML
- Use strong passwords for admin access

---

## Additional Resources

### Learning Resources

- **Tailwind CSS Documentation**: https://tailwindcss.com/docs
- **HTML Tutorial**: https://www.w3schools.com/html/
- **CSS Tutorial**: https://www.w3schools.com/css/
- **Lucide Icons**: https://lucide.dev/

### Tools

- **VS Code**: https://code.visualstudio.com/ (recommended text editor)
- **Color Picker**: https://htmlcolorcodes.com/
- **Responsive Design Tester**: https://responsively.app/
- **Web3Forms**: https://web3forms.com/ (for contact forms)

### Support

- **Stack Overflow**: https://stackoverflow.com/ (for coding questions)
- **GitHub Issues**: Report issues on your project repository
- **Community Forums**: Join web development communities for help

---

## Conclusion

You now have a comprehensive guide to maintaining and customizing your Somda landing page. Remember:

1. **Always back up** before making major changes
2. **Test thoroughly** on multiple devices and browsers
3. **Make changes incrementally** to avoid breaking things
4. **Keep content updated** to maintain relevance
5. **Follow best practices** for security and performance

If you get stuck, refer back to the specific sections in this guide, and don't hesitate to search for solutions online. Web development is a journey of continuous learning, and you're doing great!

Happy customizing! 🚀