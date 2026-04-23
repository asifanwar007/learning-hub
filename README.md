# 📚 Learning Hub - Java & Spring Boot

A unified learning platform for mastering Java and Spring Boot. **100% static website** - deploy once, update forever!

## Overview

This is a single GitHub repository with two separate learning paths:
- **☕ Java Learning** - `https://yourdomain.com/java`
- **🚀 Spring Boot Learning** - `https://yourdomain.com/spring-boot`

Both paths share the same hosting but maintain independent content.

## Features

✅ **Two Learning Paths** - Java & Spring Boot  
✅ **Responsive Design** - Mobile, tablet, desktop  
✅ **Interactive Notes** - Save locally in browser  
✅ **Code Examples** - Real, executable code  
✅ **Fast & Free** - Pure HTML/CSS/JS  
✅ **Easy Updates** - Just push to GitHub  
✅ **Single Deploy** - One GitHub repo, two learning platforms  

## Project Structure

```
learning-hub/
│
├── index.html              # Main landing page (Java + Spring Boot buttons)
│
├── java/                   # Java Learning Path
│   ├── index.html
│   ├── css/style.css
│   ├── js/script.js
│   └── pages/
│       ├── tutorial-1-basics.html
│       ├── tutorial-2-oop.html
│       ├── tutorial-3-collections.html
│       └── tutorial-4-streams.html
│
├── spring-boot/            # Spring Boot Learning Path
│   ├── index.html
│   ├── css/style.css
│   ├── js/script.js
│   └── pages/
│       ├── tutorial-1-setup.html
│       ├── tutorial-2-rest-api.html
│       ├── tutorial-3-jpa.html
│       └── tutorial-4-security.html
│
├── assets/                 # Shared assets (images, downloads)
│
├── .github/workflows/      # GitHub Actions
│
└── README.md              # This file
```

## Quick Start

### 1. Test Locally
```bash
cd learning-hub
python -m http.server 8000
# Visit: http://localhost:8000
```

### 2. Deploy to GitHub Pages

#### Step 1: Initialize Git
```bash
git init
git config user.name "Your Name"
git config user.email "your@email.com"
git add .
git commit -m "Initial commit: Learning Hub - Java & Spring Boot"
```

#### Step 2: Create GitHub Repository
1. Go to https://github.com/new
2. **Repository name**: `learning-hub`
3. Click **Create repository**

#### Step 3: Push to GitHub
```bash
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/learning-hub.git
git push -u origin main
```

#### Step 4: Enable GitHub Pages
1. Go to Settings → Pages
2. Source: **Deploy from a branch**
3. Branch: **main**
4. Folder: **/ (root)**
5. Click Save

#### Step 5: Visit Your Site
- Main hub: `https://YOUR_USERNAME.github.io/learning-hub`
- Java path: `https://YOUR_USERNAME.github.io/learning-hub/java`
- Spring Boot path: `https://YOUR_USERNAME.github.io/learning-hub/spring-boot`

## Folder Organization

### Java Learning Path
Located in `java/` folder:
- `index.html` - Java hub main page
- `css/style.css` - Java-specific styling
- `js/script.js` - Notes functionality
- `pages/` - Tutorial pages

**Access at:** `/java/` or `/java/index.html`

### Spring Boot Learning Path
Located in `spring-boot/` folder:
- `index.html` - Spring Boot hub main page
- `css/style.css` - Spring Boot styling
- `js/script.js` - Notes functionality
- `pages/` - Tutorial pages

**Access at:** `/spring-boot/` or `/spring-boot/index.html`

## How to Update

### Add Java Tutorial
1. Create: `java/pages/tutorial-5-yourname.html`
2. Link from: `java/index.html` (Tutorials section)
3. Test locally
4. Push to GitHub

### Add Spring Boot Tutorial
1. Create: `spring-boot/pages/tutorial-5-yourname.html`
2. Link from: `spring-boot/index.html` (Tutorials section)
3. Test locally
4. Push to GitHub

### Add Learning Notes
- Click "Add Note" button on any learning page
- Notes save locally in your browser
- Never lost unless you clear browser data

## Git Workflow

```bash
# Make changes to files
# Then:

git status                  # See what changed
git add .                   # Stage all changes
git commit -m "docs: add tutorial on lambdas"  # Commit
git push                    # Push to GitHub

# Changes appear live in 1-2 minutes!
```

## Customization

### Change Java Path Colors
Edit `java/css/style.css`:
```css
:root {
    --primary-color: #ed8936;      /* Orange */
    --secondary-color: #1a202c;    /* Dark */
}
```

### Change Spring Boot Colors
Edit `spring-boot/css/style.css`:
```css
:root {
    --primary-color: #6db33f;      /* Green */
    --secondary-color: #34302d;    /* Brown */
}
```

### Change Main Hub Colors
Edit `learning-hub/index.html`:
```html
<style>
    :root {
        --java-color: #ed8936;
        --spring-color: #6db33f;
    }
</style>
```

## File Organization

```
Each learning path has:
├── index.html              # Hub page for that path
├── css/style.css          # Styling (unique per path)
├── js/script.js           # Notes functionality
├── pages/                 # Tutorials
└── README.md             # Path-specific docs (optional)
```

## Relative Paths

### From Java Tutorial to Java Hub
```html
<a href="../index.html">Back to Java Home</a>
```

### From Spring Boot Tutorial to Spring Boot Hub
```html
<a href="../index.html">Back to Spring Boot Home</a>
```

### From Java/Spring Boot to Main Hub
```html
<a href="../../index.html">Back to Learning Hub</a>
```

## Deployment Variations

### Option 1: Separate GitHub Pages Domains
If you have 2 repos:
- `java-learning` repo → `yourusername.github.io/java-learning`
- `spring-boot-learning` repo → `yourusername.github.io/spring-boot-learning`

### Option 2: Single Repo (Recommended)
This repo:
- Main: `yourusername.github.io/learning-hub`
- Java: `yourusername.github.io/learning-hub/java`
- Spring Boot: `yourusername.github.io/learning-hub/spring-boot`

### Option 3: Custom Domain
With custom domain `learning.yourdomain.com`:
- Main: `learning.yourdomain.com`
- Java: `learning.yourdomain.com/java`
- Spring Boot: `learning.yourdomain.com/spring-boot`

## Maintenance

### Monthly
- [ ] Add new tutorials
- [ ] Update code examples
- [ ] Check external links

### Quarterly
- [ ] Review styling
- [ ] Update documentation
- [ ] Add new sections

## Browser Support

✅ Chrome/Edge (Latest)  
✅ Firefox (Latest)  
✅ Safari (Latest)  
✅ Mobile browsers  

## Performance

- **Fast loading** - No backend, only static files
- **Instant updates** - Push to GitHub, live in 1-2 minutes
- **No dependencies** - Pure HTML/CSS/JavaScript
- **Free hosting** - GitHub Pages included
- **Scalable** - Add unlimited pages/paths

## Troubleshooting

### Site Won't Load
- Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Clear browser cache
- Test with `python -m http.server 8000` locally

### Links Are Broken
- Check relative paths with `../`
- Verify folder structure matches paths
- Test locally before pushing

### Notes Not Saving
- Check localStorage enabled
- Open console (F12) for errors
- Try incognito/private mode

### Styles Not Applying
- Hard refresh (clear cache)
- Verify CSS file path
- Check CSS selectors match HTML classes

## Resources

- [GitHub Pages Docs](https://docs.github.com/en/pages)
- [Java Docs](https://docs.oracle.com/javase/tutorial/)
- [Spring Boot Docs](https://spring.io/projects/spring-boot)

## Next Steps

1. ✅ Set up Git locally
2. ✅ Deploy to GitHub Pages
3. ✅ Customize colors & fonts
4. ✅ Add learning content
5. ✅ Share your learning hub!

## File Checklist

Before deploying, ensure you have:

- [ ] `index.html` (main hub page)
- [ ] `java/` folder with Java learning path
- [ ] `spring-boot/` folder with Spring Boot learning path
- [ ] `.gitignore` file
- [ ] `README.md` (this file)
- [ ] All relative paths use `../`

## Example URLs

### Local Testing
```
http://localhost:8000
http://localhost:8000/java
http://localhost:8000/spring-boot
```

### GitHub Pages
```
https://yourusername.github.io/learning-hub
https://yourusername.github.io/learning-hub/java
https://yourusername.github.io/learning-hub/spring-boot
```

## Tips for Success

1. **Keep it organized** - Folder structure matters
2. **Use relative paths** - Links work locally and online
3. **Test locally first** - Before pushing to GitHub
4. **Commit regularly** - Easier to track changes
5. **Write clear commit messages** - For future reference
6. **Update content often** - Keep it fresh and relevant

## Statistics

- **Setup time**: 5 minutes
- **Deployment time**: 5 minutes
- **Update time**: < 1 minute
- **Hosting cost**: $0
- **Learning value**: ∞

## License

MIT - Free to use and modify

---

## Quick Reference

| Task | Command |
|------|---------|
| Start local server | `python -m http.server 8000` |
| Add files to git | `git add .` |
| Commit changes | `git commit -m "message"` |
| Push to GitHub | `git push` |
| Check status | `git status` |

---

Happy Learning! 📚✨

**Last Updated:** April 2026  
**Maintained by:** You  
**Status:** Active Development
