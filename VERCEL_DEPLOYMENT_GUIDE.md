# 🚀 Vercel Deployment Guide for JavaScript Mini Projects

## Quick Overview

All 4 JavaScript projects are ready to be deployed on Vercel. Each project is a standalone HTML application with no build process required.

---

## ✨ EASIEST METHOD: Create 4 Separate GitHub Repos

**This is the recommended approach** - it's simpler and Vercel works perfectly with separate repos:

### Step-by-Step Setup

#### **Create Separate Repositories**

**In your terminal (PowerShell):**

```powershell
# Create repo for Project 1: Guess the Number
cd 01-Guess-Number
git init
git add .
git commit -m "Initial commit: Guess the Number Game"
git remote add origin https://github.com/AshishCherian15/guess-the-number-game.git
git branch -M main
git push -u origin main

# Create repo for Project 2: Shopping Cart
cd ../02-Shopping-Cart
git init
git add .
git commit -m "Initial commit: Shopping Cart Calculator"
git remote add origin https://github.com/AshishCherian15/shopping-cart-calculator.git
git branch -M main
git push -u origin main

# Create repo for Project 3: View Transitions
cd ../03-View-Transitions
git init
git add .
git commit -m "Initial commit: View Transitions API Demo"
git remote add origin https://github.com/AshishCherian15/view-transitions-api-demo.git
git branch -M main
git push -u origin main

# Create repo for Project 4: URLSearchParams
cd ../04-URLSearchParams
git init
git add .
git commit -m "Initial commit: URLSearchParams Demo"
git remote add origin https://github.com/AshishCherian15/urlsearchparams-demo.git
git branch -M main
git push -u origin main
```

#### **Deploy Each Repo to Vercel**

Once you have the 4 GitHub repos created:

1. **Go to:** https://vercel.com
2. **Click "New Project"**
3. **Connect your GitHub** (if not already connected)
4. **Import repository:** `guess-the-number-game`
5. **Click "Deploy"** (No configuration needed!)
6. Copy the live URL

**Repeat for the other 3 repos:**
- `shopping-cart-calculator`
- `view-transitions-api-demo`
- `urlsearchparams-demo`

---

## 📋 Alternative Method: Deploy from Main Repo (If you prefer keeping one repo)

If you want to keep all projects in one repo, follow these steps **instead**:

### **For Single Main Repo Approach:**

1. Go to Vercel: https://vercel.com
2. Click "New Project"
3. Import: `javascript-mini-projects` 
4. **IMPORTANT - Before clicking Deploy, edit settings:**
   - Click "Edit" next to "Root Directory"
   - Set it to: `01-Guess-Number`
   - Leave Build Command empty
   - Leave Output Directory empty
5. Click "Deploy"

**Repeat for remaining projects with different Root Directories:**
- Project 2: `02-Shopping-Cart`
- Project 3: `03-View-Transitions`
- Project 4: `04-URLSearchParams`

---

## 📋 Expected Live URLs

After deployment, your URLs should look like:

```
🎮 Guess the Number Game
   https://guess-the-number-game-xxxxx.vercel.app

🛒 Shopping Cart Calculator
   https://shopping-cart-calculator-xxxxx.vercel.app

✨ View Transitions API
   https://view-transitions-api-demo-xxxxx.vercel.app

🔗 URLSearchParams Demo
   https://urlsearchparams-demo-xxxxx.vercel.app
```

---

## ⚡ TROUBLESHOOTING: If You See Configuration Errors

**Error:** "Invalid property" or "INVALID: source should NOT have additional property..."

**Solution:**
- Click **"Skip optional steps"** if Vercel shows configuration options
- Leave all build/framework settings empty
- Just click **"Deploy"** directly

The projects are static HTML - no configuration needed!

---

## ✅ Verification Checklist

After deploying all 4 projects, verify:

- [ ] **Guess Number Game**
  - [ ] Page loads without errors
  - [ ] Can enter numbers and click submit
  - [ ] Gets feedback (Too High/Low)
  - [ ] Guess history displays
  - [ ] Can reset and start new game

- [ ] **Shopping Cart**
  - [ ] Can add items with name, price, quantity
  - [ ] Cart displays in table
  - [ ] Total calculation is correct
  - [ ] Delete button works
  - [ ] Updates persist on page refresh (localStorage)

- [ ] **View Transitions**
  - [ ] Smooth animations when switching tabs
  - [ ] Home, About, Contact tabs all work
  - [ ] Content displays correctly
  - [ ] Dark/Light theme works
  - [ ] URL updates without reload

- [ ] **URLSearchParams**
  - [ ] URL parameters display in table
  - [ ] Can add/update parameters
  - [ ] Can delete parameters
  - [ ] Theme changes from URL work
  - [ ] Greeting displays correctly

---

## 🔄 Auto-Deploy from GitHub

Once deployed, Vercel automatically redeploys whenever you:
1. Push changes to GitHub
2. Make updates to the project code
3. Update any HTML/CSS/JavaScript files

Just commit and push:
```bash
git add .
git commit -m "Update projects"
git push origin main
```

Vercel will automatically rebuild and deploy! 🚀

---

## 🌐 Custom Domain (Optional)

To use a custom domain:
1. Go to Vercel project settings
2. Navigate to "Domains"
3. Add your custom domain
4. Follow DNS configuration

---

## 🆘 Troubleshooting

**Issue 1:** "Invalid property" or configuration error on Vercel
- **Solution:** 
  - Click the **back button** or **Skip this step**
  - Don't try to configure Root Directory if Vercel shows errors
  - Just click **Deploy** directly
  - These are static HTML files - no special config needed

**Issue 2:** "Cannot find index.html"
- **Solution:** Verify `index.html` exists in your project folder
  - Check: `01-Guess-Number/index.html` exists
  - Check: `02-Shopping-Cart/index.html` exists
  - Check: `03-View-Transitions/index.html` exists
  - Check: `04-URLSearchParams/index.html` exists

**Issue 3:** "Deployment fails or shows 404"
- **Solution:**
  - Make sure you're importing the correct GitHub repo
  - For separate repos: Use the correct repo name
  - For main repo: Don't use Root Directory - instead create 4 separate Vercel projects
  - Check that files are actually pushed to GitHub (git push successful)
  - Clear browser cache and refresh

**Issue 4:** "JavaScript features not working"
- **Solution:**
  - Check browser console for errors (F12 → Console tab)
  - Verify file paths are correct in HTML
  - Check that all files (HTML, CSS, JS) are included in git push
  - Test locally first: Open `index.html` in your browser directly

**Issue 5:** "localStorage not persisting"
- **Solution:**
  - This is normal on `localhost` during development
  - localStorage works fine on deployed Vercel URLs
  - Test the live Vercel deployment instead

---

## 📝 Update README with Live URLs

Once you have all 4 Vercel URLs, update the main `README.md`:

Find these lines:
```markdown
**[🎮 Play Live Demo](LIVE_DEMO_URL_1)**
**[🛍️ Try Live Demo](LIVE_DEMO_URL_2)**
**[✨ View Live Demo](LIVE_DEMO_URL_3)**
**[🌐 See Live Demo](LIVE_DEMO_URL_4)**
```

Replace with your actual URLs:
```markdown
**[🎮 Play Live Demo](https://guess-the-number-game-xxxxx.vercel.app)**
**[🛍️ Try Live Demo](https://shopping-cart-calculator-xxxxx.vercel.app)**
**[✨ View Live Demo](https://view-transitions-api-demo-xxxxx.vercel.app)**
**[🌐 See Live Demo](https://urlsearchparams-demo-xxxxx.vercel.app)**
```

Also update the live deployment table in README:
```markdown
| 🎮 Guess Number | [Play Game](https://guess-the-number-game-xxxxx.vercel.app) | ✅ Live |
| 🛒 Shopping Cart | [Try Cart](https://shopping-cart-calculator-xxxxx.vercel.app) | ✅ Live |
| ✨ View Transitions | [View Demo](https://view-transitions-api-demo-xxxxx.vercel.app) | ✅ Live |
| 🔗 URLSearchParams | [See Demo](https://urlsearchparams-demo-xxxxx.vercel.app) | ✅ Live |
```

Then commit and push:
```bash
git add README.md
git commit -m "docs: add live Vercel URLs"
git push
```

---

## 🎯 Quick Deployment Checklist

- [ ] GitHub repos created (main or separate)
- [ ] All projects pushed to GitHub
- [ ] Vercel project created for Project 1 (Guess Number)
- [ ] Vercel project created for Project 2 (Shopping Cart)
- [ ] Vercel project created for Project 3 (View Transitions)
- [ ] Vercel project created for Project 4 (URLSearchParams)
- [ ] All 4 live URLs collected
- [ ] README updated with live URLs
- [ ] Final commit to GitHub
- [ ] Let Vercel auto-redeploy
- [ ] Test all 4 live links
- [ ] Celebrate! 🎉

---

## 📚 Additional Resources

- [Vercel Docs](https://vercel.com/docs)
- [Vercel GitHub Integration](https://vercel.com/docs/platform/git-integration)
- [Deploy Static Sites on Vercel](https://vercel.com/guides)

---

**Need Help?** 
- Test locally first: Open `index.html` in your browser
- Check browser console for errors (F12)
- Check Vercel deployment logs in project settings
- Make sure index.html is in the root of each project folder

Good luck with your deployments! 🚀✨
