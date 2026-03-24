# View Transitions API

> Completed as part of **View Transitions API Essentials Workshop** — LetsUpgrade Bootcamp Program

A demo webpage that shows smooth animated transitions between different content views using the View Transitions API. Has Home, About, and Contact tabs. Clicking a tab triggers a smooth slide animation between the views using document.startViewTransition(). Includes dark/light theme and a browser fallback.

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
| `document.startViewTransition()` | Takes a callback that updates the DOM; browser animates between old and new state |
| `view-transition-name CSS` | Tells browser which element to animate with its own named transition |
| `::view-transition-old` | CSS pseudo-element targeting the outgoing/old content snapshot |
| `::view-transition-new` | CSS pseudo-element targeting the incoming/new content snapshot |
| `@keyframes animation` | Defines slideOutLeft and slideInRight animations for the transition |
| `window.history.pushState` | Updates browser URL without page reload when switching views |
| `fallback for old browsers` | Checks if startViewTransition exists before using it; falls back to direct DOM swap |
| `CSS variables` | --bg, --surface etc. change based on dark/light class on body |

---

## Core Code

```javascript
function switchView(viewName) {
  // Check browser support first
  if (!document.startViewTransition) {
    document.getElementById('content-box').innerHTML = views[viewName];
    return; // fallback - no animation
  }
  // USE THE API - browser handles the animation
  document.startViewTransition(() => {
    document.getElementById('content-box').innerHTML = views[viewName];
  });
}

/* CSS for the animation */
::view-transition-old(content-area) { animation: slideOutLeft 0.35s ease; }
::view-transition-new(content-area) { animation: slideInRight 0.35s ease; }
```

---

## Certificate

| Field | Details |
|---|---|
| Bootcamp | View Transitions API Essentials Workshop |
| Completed by | Ashish Cherian |
| Date | 12 January 2026 |
| Certificate No | LUETAPIJAN12624 |
| Verify | [www.letsupgrade.in/verify](https://www.letsupgrade.in/verify) |
| In collaboration with | NSDC, ITM Edutech, GDG MAD |

---

## Project Structure

```
02-view-transitions/
├── index.html
├── README.md
└── certificate/
    └── LUETAPIJAN12624.pdf
```

---
*Built during LetsUpgrade Bootcamp — 12 January 2026*
