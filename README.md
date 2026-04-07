# 🌸 Florissa — Handmade Flower Boutique Website

A beautiful, fully responsive multi-page website for **Florissa**, a Sri Lankan small business specialising in handmade ribbon and pipe cleaner flowers — bouquets, frames, pots, key tags, and gift sets.

---

## 🗂️ Project Structure

```
florissa/
├── index.html          # Home page
├── products.html       # All products with filter, sort & product modal
├── about.html          # About Florissa story & values
├── gallery.html        # Photo gallery with lightbox
├── contact.html        # Contact form & WhatsApp integration
├── login.html          # Login & Register page
├── cart.html           # Shopping cart with WhatsApp checkout
├── style.css           # All styling (single stylesheet)
├── logo.png            # Florissa logo image
└── images/             # Product and page images
    ├── bouquet.jpg
    ├── bouquet2.jpg
    ├── bouquet3.jpg
    ├── frame.jpg
    ├── frame2.jpg
    ├── pot.jpg
    ├── pot2.jpg
    ├── keytag.jpg
    ├── keytag2.jpg
    ├── giftset.jpg
    ├── giftset2.jpg
    ├── giftset3.jpg
    └── about.jpg
```

---

## ✨ Features

### 🛍️ Shopping
- Browse all products with **category filters** (Bouquets, Frames, Pots, Key Tags, Gift Sets)
- Filter by **material** — Ribbon or Pipe Cleaner separately
- **Sort by** Most Popular, Price Low to High, Price High to Low, Top Rated
- **Add to Cart** from any page
- **Cart with coupon codes** — BLOOM20, FRAME15, GIFT350
- **WhatsApp checkout** — order sent directly as a formatted WhatsApp message

### 📦 Product Details
- Click any product to open a **full detail modal**
- Shows product image, price, material tag, offer badge, and description
- **Star ratings + customer reviews** displayed per product
- Customers can **leave their own review** (saved in browser)
- Direct **Order on WhatsApp** button inside the modal

### 🏷️ Offers & Discounts
- Scrolling **offers ticker** on every page
- Dedicated **Offers section** on the home page with discount codes
- Discount codes applied in cart with live total recalculation
- Offer badges shown on product cards and in product modals

### 👤 Login & Register
- Simple **localStorage-based** login and registration
- No backend required — works fully in the browser
- Login state shown in navbar (Login → user name)

### 🎨 Design
- Elegant rose, cream, and brown colour palette
- **Cormorant Garamond** serif + **DM Sans** sans-serif fonts
- Circular SVG **Florissa flower logo** in navbar + brand name
- Scroll-triggered **reveal animations** on all sections
- Morphing hero image frame with floating stat cards
- **Marquee banner** and **scrolling offer ticker**
- Rotating **testimonials** with dot navigation
- Photo gallery with **hover overlay** and **lightbox viewer**
- Fully **mobile responsive** across all screen sizes

### 🔔 Notifications
- Custom **Florissa-branded notification** toast (replaces browser alerts)
- Shows logo + brand name + message — no IP address shown

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/florissa.git
cd florissa
```

### 2. Add your images

Place your product photos inside the `images/` folder using these exact filenames:

```
bouquet.jpg, bouquet2.jpg, bouquet3.jpg
frame.jpg, frame2.jpg
pot.jpg, pot2.jpg
keytag.jpg, keytag2.jpg
giftset.jpg, giftset2.jpg, giftset3.jpg
about.jpg
```

### 3. Add your logo

Place your logo file as `logo.png` in the root folder alongside the HTML files.

### 4. Set your WhatsApp number

Search for `94XXXXXXXXX` across all HTML files and replace with your real number.

Format: country code + number without leading zero.

```
Example: 0771234567 → 94771234567
```

Files to update:
- `index.html`
- `products.html`
- `about.html`
- `gallery.html`
- `contact.html`
- `login.html`
- `cart.html`

### 5. Open in browser

Simply open `index.html` in any modern browser — no server or installation needed.

```bash
# Or with VS Code Live Server extension
# Right-click index.html → Open with Live Server
```

---

## 🎁 Discount Codes

| Code | Discount | Applies To |
|------|----------|------------|
| `BLOOM20` | 20% OFF | All Bouquets |
| `FRAME15` | 15% OFF | All Frames |
| `GIFT350` | 10% OFF | Gift Sets |

To change or add codes, edit the `COUPONS` object in `cart.html`:

```javascript
const COUPONS = {
  'BLOOM20': 20,
  'FRAME15': 15,
  'GIFT350': 10
};
```

---

## 💬 WhatsApp Order Flow

When a customer clicks **Order via WhatsApp** in the cart, a pre-filled message is sent:

```
Hello Florissa! I would like to place an order:

• Ribbon Flower Bouquet ×2 — LKR 2,400
• Flower Key Tag ×1 — LKR 350

Subtotal: LKR 2,750
Discount (BLOOM20): — LKR 550
Total: LKR 2,200

Note: Please make it in pink and white.
```

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Page structure |
| CSS3 | Styling, animations, responsive layout |
| Vanilla JavaScript | Cart, filters, modals, reviews, notifications |
| localStorage | Cart, login, reviews persistence |
| Google Fonts | Cormorant Garamond + DM Sans |
| SVG | Florissa circular flower logo |
| WhatsApp API | Order placement via `wa.me` link |

---

## 📱 Browser Support

| Browser | Support |
|---|---|
| Chrome | ✅ Full |
| Firefox | ✅ Full |
| Safari | ✅ Full |
| Edge | ✅ Full |
| Mobile Chrome | ✅ Full |
| Mobile Safari | ✅ Full |

---

## 📋 Pages Overview

| Page | Description |
|---|---|
| `index.html` | Hero, offers, features, product preview, process, testimonials |
| `products.html` | Full product grid with filters, sort, and modal |
| `about.html` | Story, values, craft process, stats |
| `gallery.html` | Photo grid with filter and lightbox |
| `contact.html` | Contact info, form, WhatsApp CTA |
| `login.html` | Login and register forms |
| `cart.html` | Cart items, coupon, summary, WhatsApp order |

---

## 🌸 Customisation Guide

### Change colours
Edit the CSS variables at the top of `style.css`:

```css
:root {
  --rose: #c2606a;        /* Main pink-rose colour */
  --rose-light: #f5e0e2;  /* Light pink background */
  --rose-deep: #8b3a44;   /* Dark rose for hover */
  --cream: #faf7f2;       /* Page background */
  --brown: #4a3728;       /* Headings and text */
  --green: #6b7c5a;       /* New / accent badges */
}
```

### Add a new product
In `products.html`, copy any `product-page-card` block and update:

```html
<div class="product-page-card"
  data-category="bouquet"
  data-material="ribbon"
  data-price="1200"
  data-rating="4.8"
  data-popular="24">
```

- `data-category` — `bouquet`, `frame`, `pot`, `keytag`, `giftset`
- `data-material` — `ribbon`, `pipecleaner`
- `data-price` — price in LKR (used for sorting)
- `data-rating` — rating out of 5
- `data-popular` — number of reviews (used for popularity sort)

### Change offer codes
Edit the ticker text in the `offers-ticker` div and the offer cards in the `offers-section` on `index.html`.

---

## 👩‍💻 Developer Notes

- No frameworks, no build tools — pure HTML, CSS, and JavaScript
- All data stored in `localStorage` — clears when browser data is cleared
- Reviews are stored per product name as key in `florissaReviews`
- Cart stored as array in `florissaCart`
- Users stored as array in `florissaUsers`
- This is a **frontend-only** project — no backend, no database

---

## 📄 Licence

This project was built for **Florissa** — a handmade flower business in Sri Lanka.
All design, content, and product images belong to Florissa.
Not for redistribution or commercial reuse without permission.

---

## 🙏 Credits

- Fonts: [Google Fonts](https://fonts.google.com) — Cormorant Garamond, DM Sans
- WhatsApp integration via [wa.me](https://wa.me)
- Built with pure HTML, CSS & JavaScript — no frameworks

---

*Made with &#10022; for Florissa — Sri Lanka's handmade flower boutique*
