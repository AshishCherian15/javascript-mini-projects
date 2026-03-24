# Guess the Number Game

> Completed as part of **Make an Interactive Guess the Number Game** — LetsUpgrade Bootcamp Program

An interactive number guessing game where the computer generates a random number between 1 and 100 and the user tries to guess it. Gives Too High or Too Low feedback, tracks number of attempts, shows a narrowing range hint, logs all previous guesses, and resets with a new random number.

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
| `Math.random()` | Generates a random decimal between 0 and 1 |
| `Math.floor()` | Rounds down to whole number to get integer between 1 and 100 |
| `parseInt()` | Converts string input value to an integer for comparison |
| `if/else if/else` | Checks if guess is too high, too low, or correct |
| `DOM manipulation` | getElementById() gets elements, textContent updates text on screen |
| `event listener` | keydown event allows pressing Enter to submit guess |
| `counter variable` | attempts variable increments by 1 on each guess |
| `array + forEach` | guessHistory array stores all guesses, displayed as tags |
| `isNaN()` | Validates that user entered a number not letters |

---

## Core Code

```javascript
// Generate random number 1-100
let secretNumber = Math.floor(Math.random() * 100) + 1;

function checkGuess() {
  const userGuess = parseInt(document.getElementById('guessInput').value);
  if (isNaN(userGuess)) { /* show error */ return; }
  attempts++;
  if (userGuess > secretNumber) { /* Too High */ }
  else if (userGuess < secretNumber) { /* Too Low */ }
  else { /* Correct! */ gameOver = true; }
}

// Reset game
function resetGame() {
  secretNumber = Math.floor(Math.random() * 100) + 1;
  attempts = 0;
  /* reset UI */
}
```

---

## Certificate

| Field | Details |
|---|---|
| Bootcamp | Make an Interactive Guess the Number Game |
| Completed by | Ashish Cherian |
| Date | 5 February 2026 |
| Certificate No | LUEGNFEB12674 |
| Verify | [www.letsupgrade.in/verify](https://www.letsupgrade.in/verify) |
| In collaboration with | NSDC, ITM Edutech, GDG MAD |

---

## Project Structure

```
01-guess-the-number/
├── index.html
├── README.md
└── certificate/
    └── LUEGNFEB12674.pdf
```

---
*Built during LetsUpgrade Bootcamp — 5 February 2026*
