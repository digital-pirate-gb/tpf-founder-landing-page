# Deployment Guide - The Players Fund Founder Landing Page

## 📋 Prerequisites

- GitHub account
- Netlify account (free tier works perfectly)
- Git installed locally (✅ Already done)

## 🚀 Step 1: Create GitHub Repository

Since GitHub CLI is not installed, follow these steps to create the repository manually:

### Option A: Using GitHub Website

1. **Go to GitHub**: Visit https://github.com/new

2. **Repository Settings**:
   - **Repository name**: `tpf-founder-landing-page`
   - **Description**: The Players Fund - Premium founder landing page
   - **Visibility**: Public (or Private if preferred)
   - **DO NOT** initialize with README, .gitignore, or license (we already have these)

3. **Click "Create repository"**

4. **Connect your local repo to GitHub**:
   ```bash
   cd "Founder Landing Page"
   git remote add origin https://github.com/YOUR_USERNAME/tpf-founder-landing-page.git
   git branch -M main
   git push -u origin main
   ```
   
   Replace `YOUR_USERNAME` with your actual GitHub username.

### Option B: Using GitHub Desktop (if you have it installed)

1. Open GitHub Desktop
2. File → Add Local Repository
3. Choose the "Founder Landing Page" folder
4. Click "Publish repository"
5. Set name to `tpf-founder-landing-page`
6. Uncheck "Keep this code private" (or keep it checked if you want it private)
7. Click "Publish Repository"

## 🌐 Step 2: Deploy to Netlify

### Connect Repository to Netlify

1. **Sign in to Netlify**: Go to https://app.netlify.com

2. **Add New Site**:
   - Click "Add new site" → "Import an existing project"

3. **Connect to Git Provider**:
   - Click "GitHub"
   - Authorize Netlify to access your GitHub account
   - Select your repository: `tpf-founder-landing-page`

4. **Configure Build Settings**:
   - **Branch to deploy**: `main`
   - **Build command**: Leave empty (this is a static HTML site)
   - **Publish directory**: `.` (dot means root directory)
   - Click "Deploy site"

5. **Wait for Deployment**:
   - Netlify will automatically build and deploy your site
   - This usually takes 30-60 seconds
   - You'll get a random URL like: `https://random-name-123456.netlify.app`

## 🎯 Step 3: Custom Domain (Optional)

### Add Your Custom Domain

1. **In Netlify Dashboard**:
   - Go to Site settings → Domain management
   - Click "Add custom domain"
   - Enter your domain (e.g., `founders.theplayersfund.com`)

2. **Configure DNS**:
   
   **If using Netlify DNS (Recommended)**:
   - Netlify will provide nameservers
   - Update your domain registrar to use Netlify's nameservers
   
   **If using External DNS**:
   - Add a CNAME record:
     - Name: `founders` (or `www`)
     - Value: `your-site-name.netlify.app`
   
3. **Enable HTTPS**:
   - Netlify automatically provides free SSL certificates
   - Enable "Force HTTPS" in Domain settings

## ⚙️ Step 4: Configure Site Settings

### Environment Variables (if needed in future)
1. Go to Site settings → Environment variables
2. Add any variables you need for forms, etc.

### Form Notifications
The site uses FormSubmit.co, which works without additional configuration:
- Forms will be sent to the email specified in the HTML
- To change the email, edit `index.html` and update the form action URL

### Build & Deploy Settings
1. **Automatic Deploys**: 
   - Every push to `main` branch auto-deploys
   - You can disable this if preferred

2. **Deploy Previews**:
   - Enable deploy previews for pull requests
   - Great for testing changes before merging

## 🔄 Making Updates

### To Update Your Site:

1. **Make changes locally** to the files in "Founder Landing Page"

2. **Commit and push**:
   ```bash
   cd "Founder Landing Page"
   git add .
   git commit -m "Description of your changes"
   git push origin main
   ```

3. **Auto-deploy**:
   - Netlify detects the push
   - Automatically rebuilds and deploys
   - Live in ~1 minute

## 📊 Netlify Features You Can Use

### Analytics
- Enable Netlify Analytics to track visitors
- See page views, unique visitors, bandwidth usage

### Forms (Already Configured)
- The contact form uses FormSubmit.co
- Works without any backend configuration
- Receives email directly to specified address

### Performance
- Netlify automatically provides:
  - Global CDN
  - Asset optimization
  - Instant cache invalidation
  - DDoS protection

## 🐛 Troubleshooting

### Site Not Deploying?
- Check the Deploy log in Netlify dashboard
- Verify all files are committed to GitHub
- Ensure no build errors

### Domain Not Working?
- DNS changes can take 24-48 hours to propagate
- Verify DNS records are correct
- Check Netlify's domain configuration

### Forms Not Working?
- Verify FormSubmit.co email address is correct
- Check spam folder for form submissions
- Test form with different email addresses

## ✅ Post-Deployment Checklist

- [ ] Repository created on GitHub
- [ ] Code pushed to GitHub repository
- [ ] Site deployed to Netlify
- [ ] Site accessible via Netlify URL
- [ ] Custom domain configured (if applicable)
- [ ] HTTPS enabled
- [ ] Contact form tested
- [ ] All links verified
- [ ] Mobile responsiveness tested
- [ ] Performance tested

## 📝 Useful Commands

```bash
# Check git status
git status

# View commit history
git log --oneline

# Create a new branch for changes
git checkout -b feature/my-changes

# Return to main branch
git checkout main

# Pull latest changes
git pull origin main
```

## 🔗 Important URLs

- GitHub Repository: `https://github.com/YOUR_USERNAME/tpf-founder-landing-page`
- Netlify Dashboard: `https://app.netlify.com/sites/YOUR_SITE_NAME`
- Live Site: Will be provided after deployment

## 📞 Support

For issues with:
- **GitHub**: https://docs.github.com
- **Netlify**: https://docs.netlify.com or support@netlify.com
- **FormSubmit**: https://formsubmit.co/help

---

**🎉 That's it! Your site is now live and connected to GitHub for easy updates.**
