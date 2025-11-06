# 🚀 Quick Start - Deploy in 5 Minutes

## Step 1: Create GitHub Repository (2 minutes)

1. Go to: **https://github.com/new**

2. Fill in:
   - Repository name: `tpf-founder-landing-page`
   - Description: `The Players Fund - Founder Landing Page`
   - Choose: **Public** (recommended) or Private
   - **IMPORTANT**: Leave all checkboxes UNCHECKED (no README, no .gitignore, no license)

3. Click **"Create repository"**

## Step 2: Push Code to GitHub (1 minute)

After creating the repo, GitHub will show you commands. **Replace the commands below with your actual GitHub username:**

```bash
cd "Founder Landing Page"

# Add GitHub as remote (REPLACE YOUR_GITHUB_USERNAME)
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/tpf-founder-landing-page.git

# Push code
git branch -M main
git push -u origin main
```

**Example** (if your username is `johnsmith`):
```bash
git remote add origin https://github.com/johnsmith/tpf-founder-landing-page.git
git branch -M main
git push -u origin main
```

## Step 3: Deploy to Netlify (2 minutes)

1. Go to: **https://app.netlify.com**

2. Click: **"Add new site"** → **"Import an existing project"**

3. Click: **"GitHub"** (authorize if needed)

4. Select: **`tpf-founder-landing-page`**

5. Settings:
   - Branch: `main`
   - Build command: *leave empty*
   - Publish directory: `.` (just a dot)

6. Click: **"Deploy site"**

## ✅ Done!

Your site will be live in ~60 seconds at a URL like:
`https://random-name-123456.netlify.app`

## 🎯 Next Steps (Optional)

### Change Site Name
- Go to Site settings → Site details → Change site name
- Example: `tpf-founders` → `https://tpf-founders.netlify.app`

### Add Custom Domain
- Site settings → Domain management → Add custom domain
- Follow DNS instructions

### Update Contact Form Email
- Edit `index.html`
- Find: `action="https://formsubmit.co/`
- Update email address

## 🔄 Making Changes

After initial deploy, to update your site:

```bash
cd "Founder Landing Page"

# Make your edits to files...

git add .
git commit -m "Description of changes"
git push origin main
```

Site auto-deploys in ~60 seconds!

## 📖 Need Help?

See `DEPLOYMENT_GUIDE.md` for detailed instructions and troubleshooting.

---

**That's it! Your site is live! 🎉**
