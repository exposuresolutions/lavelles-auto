# Lavelle's Auto Diagnostics & Repair - Website & Business Suite

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)]()
[![License](https://img.shields.io/badge/license-MIT-blue)]()

**A complete digital solution for Ethan Lavelle's mechanic business on Achill Island.**

This project includes a modern, responsive website and placeholders for a full business suite, including parts ordering and Stripe payments.

## Features

- ? **Professional Branding:** Logo concept and color scheme reflecting trust and modernity.
- ? **Fully Responsive Website:** Works perfectly on desktop, tablet, and mobile.
- ? **Service-Oriented Design:** Clearly showcases services, booking, and contact info.
- ? **Online Booking Form:** A simple form to capture appointment requests.
- ? **Parts Ordering System:** A dedicated form for customers to request specific parts.
- ? **Stripe Payment Integration:** A section ready for Stripe integration to handle online invoice payments.
- ? **SEO Optimized:** Built with best practices for search engine visibility.

## Quick Start

### 1. Add Your Assets
Replace placeholder images in the `/images/` folder:
- `logo.svg` / `logo.png` - Your final logo.
- `favicon.png` - Browser favicon.
- `hero-bg.jpg` - A high-quality background image for the main section.
- `ethan-lavelle-mechanic.jpg` - A professional photo of Ethan at work.

### 2. Customize Content
Edit `index.html`:
- Update contact details (phone number, email, address).
- Refine the "About" story.
- Adjust service descriptions.

### 3. Set Up Backend & Payments

#### Booking & Parts Forms
- Connect the forms to a backend service (like GHL, a simple PHP script, or a serverless function) to receive email notifications.

#### Stripe Integration
1.  Sign up for a [Stripe account](https://stripe.com).
2.  In `js/main.js`, replace the placeholder payment logic with Stripe.js to create a payment intent and handle the transaction.
3.  You will need a server-side component to securely communicate with the Stripe API.

### 4. Deploy
Upload the website files to any web host. Recommended options:
- **Netlify / Vercel:** Excellent for static sites with easy deployment from GitHub.
- **GoHighLevel (GHL):** You can adapt the HTML/CSS/JS to a GHL site or funnel.
- **GitHub Pages:** Free hosting directly from a GitHub repository.

## File Structure

```
EthanLavelleMechanics/
??? index.html          # Main HTML file
??? css/
?   ??? style.css       # All website styles
??? js/
?   ??? main.js         # Interactive features and form handling
??? images/
?   ??? logo.svg
?   ??? ethan-lavelle-mechanic.jpg
??? README.md
```

## Branding Guide

### Logo Concept
The logo uses a strong, condensed font (`Roboto Condensed`) to convey reliability and expertise. The gear icon integrated into the "O" of "AUTO" subtly hints at the mechanical nature of the business.

### Color Palette
- **Primary Blue (`#005A9C`):** Represents trust, technology, and professionalism.
- **Accent Red (`#D40000`):** Used for calls-to-action, signifying urgency and importance.
- **Highlight Yellow (`#FDB813`):** Draws attention to key information and adds a touch of quality.
- **Dark Gray (`#1a1a1a`):** For clean, readable text.

---

This project provides a solid foundation for Ethan Lavelle to establish a strong digital presence on Achill Island.
