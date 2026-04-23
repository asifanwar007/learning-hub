# 🚀 Setup Guide - Learning Hub

Complete setup instructions for the unified Learning Hub.

## Current Status

You have created the main learning hub structure with two paths:
- **Java Learning** (`/java` folder)
- **Spring Boot Learning** (`/spring-boot` folder)

## Next Steps

### 1. Create Java Learning Content

Inside `java/` folder, you need:

```bash
java/
├── index.html           # Copy from java-learning/index.html
├── css/
│   └── style.css       # Copy from java-learning/css/style.css
├── js/
│   └── script.js       # Copy from java-learning/js/script.js
└── pages/
    ├── tutorial-1-basics.html
    ├── tutorial-2-oop.html
    ├── tutorial-3-collections.html
    └── tutorial-4-streams.html
```

**Files to copy from `/Users/asif/Music/learn/java-learning/`:**
- `index.html` → `java/index.html`
- `css/style.css` → `java/css/style.css`
- `js/script.js` → `java/js/script.js`
- All `pages/*.html` files

### 2. Create Spring Boot Learning Content

Inside `spring-boot/` folder, you need:

```bash
spring-boot/
├── index.html           # Copy from spring-boot-learning/index.html
├── css/
│   └── style.css       # Copy from spring-boot-learning/css/style.css
├── js/
│   └── script.js       # Copy from spring-boot-learning/js/script.js
└── pages/
    ├── tutorial-1-setup.html
    ├── tutorial-2-rest-api.html
    ├── tutorial-3-jpa.html
    └── tutorial-4-security.html
```

**Files to copy from `/Users/asif/Music/learn/spring-boot-learning/`:**
- `index.html` → `spring-boot/index.html`
- `css/style.css` → `spring-boot/css/style.css`
- `js/script.js` → `spring-boot/js/script.js`
- All `pages/*.html` files

### 3. Copy Commands

```bash
# Copy Java files
mkdir -p learning-hub/java/css learning-hub/java/js learning-hub/java/pages
cp java-learning/index.html learning-hub/java/
cp java-learning/css/style.css learning-hub/java/css/
cp java-learning/js/script.js learning-hub/java/js/
cp java-learning/pages/*.html learning-hub/java/pages/

# Copy Spring Boot files
mkdir -p learning-hub/spring-boot/css learning-hub/spring-boot/js learning-hub/spring-boot/pages
cp spring-boot-learning/index.html learning-hub/spring-boot/
cp spring-boot-learning/css/style.css learning-hub/spring-boot/css/
cp spring-boot-learning/js/script.js learning-hub/spring-boot/js/
cp spring-boot-learning/pages/*.html learning-hub/spring-boot/pages/
```

### 4. Update Relative Paths

After copying files, update paths in each tutorial file:

**In Java tutorials:** From `pages/tutorial-*.html`
```html
<!-- Old -->
<link rel="stylesheet" href="../css/style.css">
<script src="../js/script.js"></script>

<!-- Already correct, no change needed -->
```

**In Spring Boot tutorials:** From `pages/tutorial-*.html`
```html
<!-- Old -->
<link rel="stylesheet" href="../css/style.css">
<script src="../js/script.js"></script>

<!-- Already correct, no change needed -->
```

### 5. Test Locally

```bash
cd learning-hub
python -m http.server 8000

# Then visit:
# http://localhost:8000              # Main hub
# http://localhost:8000/java         # Java path
# http://localhost:8000/spring-boot  # Spring Boot path
```

### 6. Deploy to GitHub

```bash
cd learning-hub

# Initialize if not done
git init
git config user.name "Your Name"
git config user.email "your@email.com"

# Commit all files
git add .
git commit -m "Initial commit: Learning Hub - Java & Spring Boot"

# Create repo on github.com/new (name: learning-hub)

# Push
git remote add origin https://github.com/YOUR_USERNAME/learning-hub.git
git branch -M main
git push -u origin main
```

### 7. Enable GitHub Pages

1. Go to https://github.com/YOUR_USERNAME/learning-hub
2. Settings → Pages
3. Source: "Deploy from a branch"
4. Branch: `main`, Folder: `/ (root)`
5. Save and wait 1-2 minutes

Your site will be live at:
- Main: `https://YOUR_USERNAME.github.io/learning-hub`
- Java: `https://YOUR_USERNAME.github.io/learning-hub/java`
- Spring Boot: `https://YOUR_USERNAME.github.io/learning-hub/spring-boot`

## Folder Structure Recap

```
learning-hub/                          ← GitHub Repository
│
├── index.html                         ← Main landing (Java + Spring Boot)
├── README.md                          ← Main documentation
│
├── java/                             ← Java Learning Hub
│   ├── index.html
│   ├── css/style.css
│   ├── js/script.js
│   └── pages/
│       ├── tutorial-1-basics.html
│       ├── tutorial-2-oop.html
│       ├── tutorial-3-collections.html
│       └── tutorial-4-streams.html
│
├── spring-boot/                      ← Spring Boot Learning Hub
│   ├── index.html
│   ├── css/style.css
│   ├── js/script.js
│   └── pages/
│       ├── tutorial-1-setup.html
│       ├── tutorial-2-rest-api.html
│       ├── tutorial-3-jpa.html
│       └── tutorial-4-security.html
│
├── assets/                           ← Shared assets (images, etc.)
│
└── .gitignore                        ← Git ignore file
```

## Key Points

✅ **Single Repository** - Both Java and Spring Boot in one GitHub repo  
✅ **Independent Paths** - Each has its own CSS, JS, and pages  
✅ **Easy Navigation** - Main hub links to both learning paths  
✅ **Shared Hosting** - Deploy once, update both paths  
✅ **Modular Structure** - Easy to add more learning paths later  

## Update Workflow

### To add a new Java tutorial:
```bash
# 1. Create file
touch learning-hub/java/pages/tutorial-5-yourname.html

# 2. Edit file and add link to java/index.html

# 3. Test locally
python -m http.server 8000

# 4. Commit and push
git add .
git commit -m "docs: add Java tutorial on X"
git push
```

### To add a new Spring Boot tutorial:
```bash
# Same as above, but in spring-boot/ folder
```

## Troubleshooting

### Links to tutorial pages not working?
- Check relative paths: `pages/tutorial-*.html`
- Verify file names match exactly
- Test locally first

### CSS/JS not loading?
- Hard refresh: Ctrl+Shift+R
- Check file paths in HTML
- Verify files exist in correct folders

### Pages not showing on GitHub?
- Wait 2-3 minutes for deployment
- Hard refresh browser
- Check GitHub Pages status in Settings

## Tips

1. **Keep folder structure clean** - Easier to maintain
2. **Use consistent naming** - Lowercase, hyphens for files
3. **Test locally before pushing** - Avoid broken links on live site
4. **Write clear commit messages** - For documentation
5. **Update regularly** - Keep content fresh

## Estimated Setup Time

- **Copy files**: 2 minutes
- **Test locally**: 1 minute
- **Deploy to GitHub**: 5 minutes
- **Enable Pages**: 2 minutes
- **Total**: ~10 minutes

## Done! ✅

You now have:
- ✅ Unified learning hub
- ✅ Java learning path
- ✅ Spring Boot learning path
- ✅ GitHub-ready structure
- ✅ Easy to update and maintain

**Next:** Deploy to GitHub and share your learning hub!

---

For detailed info, see:
- `README.md` - Complete documentation
- `java/` - Java learning resources
- `spring-boot/` - Spring Boot learning resources
