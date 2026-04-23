# 📤 Deployment Guide - Learning Hub

Deploy your unified Learning Hub to GitHub Pages in 10 minutes.

## Prerequisites

- GitHub account (free at github.com)
- Git installed on your computer
- All files set up in `learning-hub/` folder

## Quick Deploy (5 Steps)

### Step 1: Initialize Git

```bash
cd learning-hub
git init
```

### Step 2: Configure Git

```bash
git config user.name "Your Name"
git config user.email "your@email.com"
```

### Step 3: Commit Files

```bash
git add .
git commit -m "Initial commit: Learning Hub - Java & Spring Boot"
```

### Step 4: Create GitHub Repository

1. Go to https://github.com/new
2. **Repository name**: `learning-hub`
3. **Description**: "Java & Spring Boot Learning Hub"
4. Choose **Public**
5. Click **Create repository**

### Step 5: Push to GitHub

GitHub will show commands to run:

```bash
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/learning-hub.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username.

## Enable GitHub Pages

1. Go to https://github.com/YOUR_USERNAME/learning-hub
2. Click **Settings** (top right)
3. Click **Pages** (left sidebar)
4. Under "Source":
   - Select **Deploy from a branch**
   - Choose **main** branch
   - Choose **/ (root)** folder
5. Click **Save**

You'll see: "Your site is live at https://YOUR_USERNAME.github.io/learning-hub"

Wait 1-2 minutes for deployment to complete.

## Live URLs

Once deployed:

| Path | URL |
|------|-----|
| Main Hub | `https://YOUR_USERNAME.github.io/learning-hub` |
| Java Learning | `https://YOUR_USERNAME.github.io/learning-hub/java` |
| Spring Boot Learning | `https://YOUR_USERNAME.github.io/learning-hub/spring-boot` |

## Update After Deployment

Any changes push automatically:

```bash
# Make changes to files...

# Then:
git add .
git commit -m "docs: add new tutorial"
git push

# Changes appear live in 1-2 minutes!
```

## Test Before Deploying

Always test locally first:

```bash
cd learning-hub
python -m http.server 8000

# Visit http://localhost:8000 and test all links
```

## Verify Deployment

1. Go to your GitHub repo
2. Click on "Deployments" tab
3. Check status of latest deployment
4. Should show "Success" with green checkmark

## Troubleshooting

### Site Shows 404

**Cause:** Pages not deployed yet or wrong branch selected

**Solution:**
- Wait 2-3 minutes
- Hard refresh browser
- Check Pages settings (Settings → Pages)

### Old Content Showing

**Cause:** Browser cache

**Solution:**
- Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Clear browser cache
- Try different browser

### Files Not Found

**Cause:** Wrong relative paths or missing files

**Solution:**
- Check file structure matches
- Verify relative paths use `../`
- Test locally with `python -m http.server 8000`

### Changes Not Showing

**Cause:** Not pushed to GitHub or cache issue

**Solution:**
```bash
git status  # Check what's staged
git push    # Push again
```
- Wait 1-2 minutes
- Hard refresh browser

## Folder Structure Check

Verify before deploying:

```
learning-hub/
├── index.html                 ✓
├── README.md                  ✓
├── DEPLOY.md                  ✓
├── .gitignore                 ✓
│
├── java/
│   ├── index.html            ✓
│   ├── css/style.css         ✓
│   ├── js/script.js          ✓
│   └── pages/
│       ├── tutorial-1-basics.html        ✓
│       ├── tutorial-2-oop.html          ✓
│       ├── tutorial-3-collections.html  ✓
│       └── tutorial-4-streams.html      ✓
│
└── spring-boot/
    ├── index.html            ✓
    ├── css/style.css         ✓
    ├── js/script.js          ✓
    └── pages/
        ├── tutorial-1-setup.html        ✓
        ├── tutorial-2-rest-api.html     ✓
        ├── tutorial-3-jpa.html         ✓
        └── tutorial-4-security.html     ✓
```

## Final Checklist

Before going live:

- [ ] All files copied to correct folders
- [ ] Tested locally with `python -m http.server 8000`
- [ ] All links work (click every link, test navigation)
- [ ] Git initialized and committed
- [ ] Repository created on GitHub
- [ ] Files pushed to GitHub
- [ ] GitHub Pages enabled
- [ ] Waited 2-3 minutes for deployment

## Post-Deployment

### Share Your Site

- Tell friends the URL
- Add to your resume/portfolio
- Share on social media
- Show your learning progress

### Keep it Updated

```bash
# Weekly
- Add learning notes
- Fix any issues
- Update content

# Monthly
- Add new tutorials
- Update examples
- Review and refresh content

# Quarterly
- Major updates
- New sections
- Performance improvements
```

### Monitor Performance

GitHub Pages shows:
- Deployment status
- Page views (if enabled)
- Build logs

## Advanced Options

### Custom Domain

To use `learning.yourdomain.com`:

1. Buy domain (GoDaddy, Namecheap, etc.)
2. In GitHub Pages settings, add custom domain
3. Update DNS records at domain provider

### Use GitHub Actions for CI/CD

Optional: Add automated checks before deploy

```yaml
# .github/workflows/validate.yml
name: Validate HTML
on: [push]
jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Validate HTML files
        run: |
          # Add validation commands here
```

## Statistics

- **Deploy time**: ~10 minutes
- **Update time**: < 1 minute
- **Downtime**: 0 minutes
- **Hosting cost**: $0
- **Learning value**: ∞

## Deployment Workflow

```
Local Development
    ↓
Test with python -m http.server 8000
    ↓
Commit: git add . && git commit -m "message"
    ↓
Push: git push
    ↓
GitHub deploys automatically
    ↓
Live in 1-2 minutes!
```

## Success Indicators

✅ Repository created  
✅ All files pushed  
✅ Pages enabled  
✅ Deployment successful  
✅ Site accessible  
✅ All links work  
✅ Mobile responsive  

## Getting Help

| Issue | Check |
|-------|-------|
| Site won't load | GitHub Pages settings |
| Links broken | Relative paths, file names |
| Styles missing | Check CSS file path |
| Notes not saving | Browser localStorage |
| Pages won't update | Git push, wait 2 min, refresh |

## Next Steps After Deploy

1. ✅ Test every link in your site
2. ✅ Share URL with friends
3. ✅ Add to your portfolio
4. ✅ Keep updating with new content
5. ✅ Enjoy your learning journey!

---

**You're ready to deploy!** 🚀

For more info, see:
- `README.md` - Complete documentation
- `SETUP.md` - Setup instructions
- GitHub Pages docs: https://docs.github.com/en/pages
