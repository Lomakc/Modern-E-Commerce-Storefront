# AURA | Modern Lifestyle & Essentials Storefront

A modern, responsive, client-side e-commerce storefront built with clean HTML5, Tailwind CSS, and vanilla JavaScript. The project demonstrates real-world online shopping features including catalog filtering, instant live search, sliding cart management, promo code validation, and simulated checkout.

---

## 🚀 Features

- **Responsive Design:** Fully responsive layout with mobile drawer navigation, flexible grids, and mobile-optimized search.
- **Dynamic Product Catalog:**
  - Real-time instant search by title, category, and description.
  - Category pill filter tabs (`All`, `Electronics`, `Fashion`, `Home & Living`, `Accessories`).
  - Multi-criteria sorting (Featured, Price: Low to High, Price: High to Low, Top Rated).
- **Interactive Slide-Over Cart Drawer:**
  - Dynamic item quantity adjustment (+ / -) and deletion.
  - Interactive free shipping progress tracker ($150 target).
  - Promo code discounts engine (built-in promo code: `SAVE10` for 10% off).
  - Automated itemized calculation (Subtotal, 8% Sales Tax, Shipping, Total).
  - Cart persistence via browser `localStorage`.
- **Product Quick-View Modal:** Detailed product preview including ratings, stock status, and express addition to bag.
- **Wishlist Toggle:** Save and remove favorite items with dynamic badge indicators.
- **Toast Notification System:** Non-intrusive alerts for user feedback on cart and wishlist actions.
- **Simulated Checkout Flow:** Modal confirmation showcasing generated order tracking numbers and itemized totals.

---

## 📁 File Structure

```text
├── index.html       # Complete single-file application (HTML, Tailwind CSS, JavaScript)
└── README.md        # Project documentation and setup guide
```

---

## 🛠️ Tech Stack & Dependencies

- **HTML5:** Semantic markup and structure.
- **Tailwind CSS (v3 CDN):** Utility-first styling framework with configured custom brand color palettes.
- **Vanilla JavaScript (ES6+):** Pure client-side reactive state management without heavyweight dependencies.
- **FontAwesome (v6 CDN):** Icon pack for cart, search, actions, and stars.
- **Google Fonts:** Plus Jakarta Sans typography.

---

## ⚡ Getting Started

### 1. Direct Execution
No build tools, compilation, or package installations are required.

1. Clone or download the repository files:
   ```bash
   git clone https://github.com/your-username/aura-shopping-storefront.git
   cd aura-shopping-storefront
   ```
2. Double-click `index.html` or open it with your web browser:
   ```bash
   open index.html   # On macOS
   start index.html  # On Windows
   xdg-open index.html # On Linux
   ```

### 2. Live Server (Recommended for local dev)
If using VS Code, install the **Live Server** extension, right-click `index.html`, and choose **"Open with Live Server"**.

Alternatively, run with Python:
```bash
# Python 3
python -m http.server 8000
```
Then navigate to `http://localhost:8000` in your browser.

---

## 🏷️ Demo Promo Codes

| Promo Code | Discount | Note |
| :--- | :--- | :--- |
| `SAVE10` | 10% off entire subtotal | Enter into the cart drawer promo field |

---

## 🧩 Customization Guide

### Adding New Products
Locate the `products` array inside the `<script>` tag in `index.html`:

```javascript
{
  id: 9,
  title: "Your Product Name",
  category: "Electronics", // Must match one of the categories
  price: 99.00,
  originalPrice: 129.00,
  rating: 4.8,
  reviewsCount: 30,
  isFeatured: true,
  tag: "New",
  image: "https://your-image-url.jpg",
  description: "Detailed description of the product."
}
```

### Modifying Tax & Free Shipping Thresholds
Inside `updateCartUI()` in `index.html`:
- **Free Shipping Threshold:** Adjust `const freeShippingThreshold = 150;`
- **Sales Tax Rate:** Adjust `const tax = taxableSubtotal * 0.08;` (default is 8%)
- **Flat Shipping Cost:** Adjust `const shipping = isFreeShipping ? 0 : 15.00;`

---

## 📄 License
This project is open-source and free to use for personal, educational, or commercial storefront projects.
