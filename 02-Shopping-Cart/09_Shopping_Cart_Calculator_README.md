# Shopping Cart Calculator

> Completed as part of **Shopping Cart Calculator Essentials: Local Storage & Responsive UI** — LetsUpgrade Bootcamp Program

A shopping cart calculator where users can add products with name, price, and quantity. Displays all cart items in a table with per-item totals, shows grand total and item count summary, and saves the cart to localStorage so it persists after page refresh. Includes smart duplicate detection.

---

## Live Demo

[Add your live demo link here — deploy on Vercel or GitHub Pages]

---

## Screenshots

| View 1 | View 2 |
|---|---|
| ![Screenshot 1](screenshots/1.png) | ![Screenshot 2](screenshots/2.png) |

---

## Tech Used

- HTML5
- CSS3
- JavaScript

---

## How to Run

1. Download `index.html`
2. Open in VS Code
3. Right-click and select **Open with Live Server**

---

## Key Concepts

| Concept | Purpose |
|---|---|
| `localStorage.setItem()` | Saves cart array as JSON string to browser storage |
| `localStorage.getItem()` | Reads saved cart JSON string on page load |
| `JSON.stringify()` | Converts JavaScript array to JSON string for storage |
| `JSON.parse()` | Converts JSON string back to JavaScript array |
| `parseFloat() + parseInt()` | Converts string inputs to numbers for price and quantity calculations |
| `Array.reduce()` | Calculates grand total by summing all item totals in one line |
| `DOM table manipulation` | Creates tr and td elements dynamically for each cart item |
| `duplicate detection` | Checks if item name already exists in cart and updates qty instead of adding duplicate |
| `e.stopPropagation()` | Prevents delete button click from bubbling to parent row event |

---

## Core Code

```javascript
// Save to localStorage
function saveCart() {
  localStorage.setItem('shopping-cart', JSON.stringify(cart));
}

// Load from localStorage on page start
let cart = JSON.parse(localStorage.getItem('shopping-cart')) || [];

// Calculate grand total
const grandTotal = cart.reduce((sum, item) => sum + item.total, 0);

// Check for duplicate before adding
const existing = cart.find(item => item.name.toLowerCase() === name.toLowerCase());
if (existing) { existing.qty += qty; existing.total = existing.price * existing.qty; }
else { cart.push({ id:Date.now(), name, price, qty, total:price*qty }); }
```

---

## Certificate

| Field | Details |
|---|---|
| Bootcamp | Shopping Cart Calculator Essentials: Local Storage & Responsive UI |
| Completed by | Ashish Cherian |
| Date | 2 February 2026 |
| Certificate No | LUESCCFEB12613 |
| Verify | [www.letsupgrade.in/verify](https://www.letsupgrade.in/verify) |
| In collaboration with | NSDC, ITM Edutech, GDG MAD |

---

## Project Structure

```
03-shopping-cart/
├── index.html
├── README.md
└── certificate/
    └── LUESCCFEB12613.pdf
```

---
*Built during LetsUpgrade Bootcamp — 2 February 2026*
