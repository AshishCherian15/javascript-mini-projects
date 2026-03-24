# URLSearchParams Demo

> Completed as part of **URL SearchParams Essentials: Modern JS Mini Workshop** — LetsUpgrade Bootcamp Program

A demo webpage that reads, adds, updates, and removes URL query parameters using the URLSearchParams API. Shows current URL params in a table, provides buttons to modify them live, applies theme from URL parameter, and displays personalized greeting from name parameter. Demonstrates real-world URL-driven page behavior.

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
| `new URLSearchParams(window.location.search)` | Creates URLSearchParams object from current URL's query string |
| `params.get(key)` | Reads the value of a specific parameter from the URL |
| `params.set(key,value)` | Updates an existing parameter or adds it if not present |
| `params.append(key,value)` | Adds a new parameter without replacing existing ones |
| `params.delete(key)` | Removes a parameter from the URL |
| `params.toString()` | Converts params back to query string format for URL |
| `window.history.pushState` | Updates URL in browser bar without reloading the page |
| `params.entries()` | Returns all key-value pairs from the params for looping |

---

## Core Code

```javascript
// Get params from current URL
const params = new URLSearchParams(window.location.search);

// Read a parameter
const name = params.get('name'); // 'Rahul' or null
const theme = params.get('theme') || 'light'; // default to 'light'

// Modify params
params.set('course', 'javascript'); // add/update
params.delete('city'); // remove

// Update URL without page reload
window.history.pushState({}, '', '?' + params.toString());
```

---

## Certificate

| Field | Details |
|---|---|
| Bootcamp | URL SearchParams Essentials: Modern JS Mini Workshop |
| Completed by | Ashish Cherian |
| Date | 27 January 2026 |
| Certificate No | LUEURLSPJAN12623 |
| Verify | [www.letsupgrade.in/verify](https://www.letsupgrade.in/verify) |
| In collaboration with | NSDC, ITM Edutech, GDG MAD |

---

## Project Structure

```
04-urlsearchparams/
├── index.html
├── README.md
└── certificate/
    └── LUEURLSPJAN12623.pdf
```

---
*Built during LetsUpgrade Bootcamp — 27 January 2026*
