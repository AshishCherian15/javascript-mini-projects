# 🚀 Vercel Deployment Guide for JavaScript Mini Projects

## Quick Overview

All 4 JavaScript projects are ready to be deployed on Vercel. Each project is a standalone HTML application with no build process required.

---

## 🎯 Deployment Methods

### **Method 1: Vercel Dashboard (Recommended)**

#### Step 1: Create 4 Separate GitHub Repositories (Optional but Recommended)

For better organization, you can create separate repos for each project:

```bash
# Create repo for Project 1
cd 01-Guess-Number
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/AshishCherian15/guess-the-number-game.git
git push -u origin master

# Repeat for each project with different repo names:
# - shopping-cart-calculator
# - view-transitions-api-demo
# - urlsearchparams-demo
```

**OR**

#### Step 2: Deploy Directly from Main Repo (Easier)

1. **Go to Vercel Dashboard:** https://vercel.com
2. **Click "New Project"**
3. **Import your GitHub repo:** `javascript-mini-projects`
4. **Configure each deployment:**

### **For Each Project - Configuration Steps:**

#### **Project 1: Guess the Number Game**

1. Click "New Project" on Vercel
2. Select: `javascript-mini-projects`
3. **Project Settings:**
   - **Project Name:** `guess-the-number-game`
   - **Root Directory:** `01-Guess-Number`
   - **Build Command:** Leave empty (No build needed)
   - **Output Directory:** Leave empty or `.`

4. Click "Deploy"
5. **After Deploy:** Copy the live URL (will be like `https://guess-the-number-game-xxxxx.vercel.app`)

#### **Project 2: Shopping Cart**

1. Click "New Project" 
2. Select: `javascript-mini-projects`
3. **Project Settings:**
   - **Project Name:** `shopping-cart-calculator`
   - **Root Directory:** `02-Shopping-Cart`
   - **Build Command:** Leave empty
   - **Output Directory:** Leave empty or `.`

4. Deploy and copy URL

#### **Project 3: View Transitions API**

1. Click "New Project"
2. Select: `javascript-mini-projects`
3. **Project Settings:**
   - **Project Name:** `view-transitions-api-demo`
   - **Root Directory:** `03-View-Transitions`
   - **Build Command:** Leave empty
   - **Output Directory:** Leave empty or `.`

4. Deploy and copy URL

#### **Project 4: URLSearchParams**

1. Click "New Project"
2. Select: `javascript-mini-projects`
3. **Project Settings:**
   - **Project Name:** `urlsearchparams-demo`
   - **Root Directory:** `04-URLSearchParams`
   - **Build Command:** Leave empty
   - **Output Directory:** Leave empty or `.`

4. Deploy and copy URL

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

## ✅ Verification Checklist

After deploying all 4 projects, verify:

- [ ] **Guess Number Game**
  - [ ] Page loads without errors
  - [ ] Can enter numbers
  - [ ] Gets feedback (Too High/Low)
  - [ ] Guess history displays

- [ ] **Shopping Cart**
  - [ ] Can add items
  - [ ] Cart displays in table
  - [ ] Updates persist on refresh (localStorage)
  - [ ] Delete button works

- [ ] **View Transitions**
  - [ ] Smooth animations when switching tabs
  - [ ] Home, About, Contact tabs responsive
  - [ ] Dark/Light theme works
  - [ ] URL updates without reload

- [ ] **URLSearchParams**
  - [ ] URL parameters display in table
  - [ ] Can add/update parameters
  - [ ] Theme changes from URL work
  - [ ] Greeting displays correctly

---

## 🔄 Auto-Deploy from GitHub

Once deployed, Vercel automatically redeploys whenever you:
1. Push changes to GitHub
2. Make updates to the main README
3. Update any project code

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

**Issue:** "No framework detected"
- **Solution:** Normal for static HTML. Leave all build settings empty.

**Issue:** "Cannot find index.html"
- **Solution:** Ensure `index.html` is in the root directory of each project folder.

**Issue:** "Deployment fails"
- **Solution:** 
  - Check that files are pushed to GitHub
  - Verify Root Directory path is correct
  - Clear cache and redeploy

**Issue:** "JavaScript features not working"
- **Solution:**
  - Check browser console for errors (F12)
  - Verify file paths are correct
  - Check for CORS issues (unlikely for localhost, but possible on deployed version)

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

Also update the live deployment table:
```markdown
| 🎮 Guess Number | [Play Game](https://guess-the-number-game-xxxxx.vercel.app) | ✅ Live |
| 🛒 Shopping Cart | [Try Cart](https://shopping-cart-calculator-xxxxx.vercel.app) | ✅ Live |
| ✨ View Transitions | [View Demo](https://view-transitions-api-demo-xxxxx.vercel.app) | ✅ Live |
| 🔗 URLSearchParams | [See Demo](https://urlsearchparams-demo-xxxxx.vercel.app) | ✅ Live |
```

---

## 🎯 Next Steps

1. ✅ Local folder structure organized
2. ✅ HTML files renamed to index.html
3. ✅ Enhanced README created
4. ✅ GitHub repository initialized and pushed
5. **🔄 Deploy all 4 projects on Vercel** ← You are here
6. Update README with live URLs
7. Final commit and celebrate! 🎉

---

## 📚 Additional Resources

- [Vercel Docs](https://vercel.com/docs)
- [Deploy Static HTML on Vercel](https://vercel.com/docs/platform/build-output-api#static-files)
- [Vercel GitHub Integration](https://vercel.com/docs/platform/git-integration)

---

**Need Help?** 
- Check Vercel logs: Project → Settings → Deployments
- Test locally first: Open `01-Guess-Number/index.html` in browser
- Check browser console for JavaScript errors (F12)

Good luck with your deployments! 🚀✨
