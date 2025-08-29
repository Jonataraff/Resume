# GitHub Pages Deployment Guide

This guide explains how to deploy your portfolio on GitHub Pages to make it available online for free.

## 📋 Prerequisites

- GitHub account
- Repository created on GitHub
- Portfolio code already committed

## 🚀 Deployment Steps

### 1. Upload Code

1. **Create repository on GitHub:**
   - Go to [github.com](https://github.com)
   - Click "New repository"
   - Suggested name: `portfolio` or `my-portfolio`
   - Make it public
   - DO NOT initialize with README (we already have one)

2. **Connect local repository:**
   ```bash
   git remote add origin https://github.com/YOUR-USERNAME/REPO-NAME.git
   git branch -M main
   git push -u origin main
   ```

### 2. Enable GitHub Pages

1. **Access settings:**
   - Go to your repository on GitHub
   - Click the "Settings" tab
   - Scroll down to find "Pages" in the sidebar

2. **Configure Pages:**
   - In "Source", select "Deploy from a branch"
   - In "Branch", select "main"
   - In "Folder", leave "/ (root)"
   - Click "Save"

3. **Wait for deployment:**
   - GitHub will take a few minutes to deploy
   - You'll see a green message when ready
   - Site will be available at: `https://YOUR-USERNAME.github.io/REPO-NAME`

### 3. Configure Custom Domain (Optional)

If you have your own domain:

1. **Add CNAME file:**
   ```bash
   echo "yourdomain.com" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

2. **Configure DNS:**
   - In your domain provider, add a CNAME record
   - Point to: `YOUR-USERNAME.github.io`

## 🔄 Updates

To update the site:

```bash
# Make your changes to the code
git add .
git commit -m "Description of changes"
git push
```

GitHub Pages will automatically update in a few minutes.

## 🛠️ Useful Commands

```bash
# Check repository status
git status

# View commit history
git log --oneline

# Create new branch for testing
git checkout -b new-feature

# Return to main branch
git checkout main

# Merge branch
git merge new-feature
```

## 📱 Verify Deployment

After deployment, test:

- ✅ Site loads correctly
- ✅ All sections work
- ✅ External links open
- ✅ Mobile responsiveness
- ✅ Smooth navigation works
- ✅ **Dark mode toggle functions properly**
- ✅ **Theme persistence works**

## 🔧 Troubleshooting

### Site doesn't load
- Check if file is named `index.html`
- Confirm it's in the repository root
- Wait up to 10 minutes after push

### CSS/JS doesn't work
- Verify paths are correct
- Use relative paths (without `/` at start)
- CDNs should use HTTPS

### 404 Error
- Confirm repository is public
- Check if GitHub Pages is enabled
- Test correct link: `https://YOUR-USERNAME.github.io/REPO-NAME`

## 📊 Monitoring

- **Analytics:** Add Google Analytics to monitor visits
- **Performance:** Use PageSpeed Insights for optimization
- **SEO:** Configure meta tags for better indexing

## 🔒 Security

- Never commit sensitive information
- Use environment variables for APIs
- Keep dependencies updated

## 🌙 Dark Mode Notes

Your portfolio includes a complete dark mode implementation:
- Theme preference is saved in localStorage
- Respects system preference on first visit
- All elements transition smoothly between themes
- Proper contrast ratios maintained in both modes

---

🎉 **Congratulations!** Your portfolio is online and professional!

