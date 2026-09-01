# Shi (Billy) Chen's Personal Homepage

A world-class academic homepage showcasing research, entrepreneurial experience, and achievements. **Ready to deploy!**

## Table of Contents
- [Quick Start](#quick-start)
- [Media Files](#media-files)
- [Testing Locally](#testing-locally)
- [Deploying Your Site](#deploying-your-site)
- [Customizing Content](#customizing-content)
- [Favicon](#favicon)
- [Common Questions](#common-questions)

---

## Quick Start

Your homepage is **complete and ready to deploy!** All media files are in place.

### Test Locally (Recommended First Step)

```bash
cd /home/cs/Home_Page/shi_chen_homepage
python3 -m http.server 8000
# Open http://localhost:8000 in your browser
```

**Why use a local server?**
- Videos will play correctly
- Tests exactly how site will work when deployed
- Better for testing all interactive features

---

## Media Files

### ✅ All Media Complete!

Your homepage includes a mix of images and videos for maximum impact:

#### **Profile & Logos**
- ✅ `ShiChen.jpg` (5.4M) - Profile photo
- ✅ `Fudan_University_Logo.svg` - University logo (SVG, clickable)
- ✅ `Seal_of_University_of_California,_Berkeley.svg` - University logo (SVG, clickable)
- ✅ `intuition_logo.png` - Company logo (clickable to website)

#### **Research Projects - Interactive Media**

**1. LiDAR Segmentation** (Highlighted, with hover effect)
- Default: `lidar_after.mp4` (38M) - Your results, autoplay loop 🎬
- Hover: `lidar_before.mp4` (22M) - Baseline comparison 🎬

**2. Mesh Optimization** (Highlighted, with hover effect)
- Default: `mesh_after.mp4` (3.7M) - Optimized mesh, autoplay loop 🎬
- Hover: `mesh_before.mp4` (3.9M) - Baseline mesh 🎬

**3. Drone Navigation** (with hover effect)
- Default: `drone_before.mp4` (7.2M) - Flying action, autoplay loop 🎬
- Hover: `drone_after.png` (928K) - Static image 📸

**4. Hand Generation** (static)
- `hand.png` (11M) - Single image, no hover 📸

**5. Autonomous Driving** (static)
- `av.png` (12M) - Single image, no hover 📸

**6. Stateful Agent** (static)
- `stateful_agent.jpg` (362K) - Project screenshot 📸
- Links to GitHub repos (hidden URLs)

### Interactive Hover Effects

Projects show **impressive results by default**, then reveal baseline/comparison **on hover**. This immediately impresses visitors without requiring interaction.

---

## Testing Locally

### Option 1: Local Server (Recommended)
```bash
cd /home/cs/Home_Page/shi_chen_homepage
python3 -m http.server 8000
# Open http://localhost:8000
```

### Option 2: Simple Browser Open
```bash
cd /home/cs/Home_Page/shi_chen_homepage
firefox index.html
# or
google-chrome index.html
```

**Note:** Videos work best with a local server.

---

## Deploying Your Site

### GitHub Pages (Recommended - Free)

**Step 1: Create Repository**
1. Go to [github.com](https://github.com)
2. Create new repository named: `YOUR_USERNAME.github.io`
3. Make it **public**

**Step 2: Push Your Code**
```bash
cd /home/cs/Home_Page/shi_chen_homepage
git init
git add .
git commit -m "Initial commit: Personal homepage"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_USERNAME.github.io.git
git push -u origin main
```

**Step 3: Done!**
- Your site will be live at: `https://YOUR_USERNAME.github.io`
- Updates automatically when you push changes
- Free SSL certificate included
- Custom domain support available

### Other Deployment Options
- **Netlify:** Drag and drop the folder
- **Vercel:** Connect GitHub repo for auto-deploy
- **Custom Server:** Upload files to any web host

---

## Customizing Content

### Updating Your Bio
**Location:** Lines ~31-39 in `index.html`

```html
<p>
I'm a final-year undergraduate at <a href="https://www.fudan.edu.cn/en/">Fudan University</a>...
</p>
```

### Adding News Items
**Location:** Around line 52 in `index.html`

```html
<li><strong>[Date]</strong> Your news item here</li>
```

Keep to 4-6 most recent items for clean appearance.

### Adding a Research Project

**For projects with hover effects:**
1. Copy an existing project `<tr>...</tr>` block with hover
2. Replace unique ID (e.g., `lidar` → `newproject`)
3. Update JavaScript function names (4 instances)
4. Add your media files: `newproject_after` and `newproject_before`
5. Update title, authors, description, links

**For projects with single media:**
1. Copy the Hand or AV project structure (no hover)
2. Update content and add single image

### Highlighting Important Projects

Add yellow background to make projects stand out:

```html
<tr style="background-color: #ffffd0;">
```

Currently highlighted: LiDAR and Mesh projects.

### Changing Colors

**Location:** `stylesheet.css`

```css
/* Line 67 - Link color */
a { color: #1772d0; }

/* Line 73 - Hover color */
a:hover { color: #f09228; }

/* Line 134 - Highlight background */
span.highlight { background-color: #ffffd0; }
```

---

## Favicon

### ✅ Custom Favicon Active

Your custom favicon appears in:
- Browser tabs
- Bookmarks
- Mobile home screens
- Search results
- PWA installations

**Files:** `images/favicon/`
- `favicon.ico` - Classic format
- `favicon.svg` - Modern scalable format
- `favicon-96x96.png` - High quality PNG
- `apple-touch-icon.png` - iOS devices
- `site.webmanifest` - PWA configuration

### To Update Favicon
1. Create design (512x512px recommended)
2. Use [RealFaviconGenerator](https://realfavicongenerator.net/)
3. Replace files in `images/favicon/`
4. Clear browser cache

---

## File Structure

```
shi_chen_homepage/
├── index.html              # Main homepage (400+ lines)
├── stylesheet.css          # Jon Barron's template styling
├── README.md              # This file
├── data/
│   └── Shi_Chen_Resume.pdf  # Resume (built from Resume/latex/resume.tex)
└── images/
    ├── ShiChen.jpg        # Profile photo
    ├── Fudan_University_Logo.svg
    ├── Seal_of_University_of_California,_Berkeley.svg
    ├── intuition_logo.png
    ├── lidar_after.mp4    # Research videos
    ├── lidar_before.mp4
    ├── mesh_after.mp4
    ├── mesh_before.mp4
    ├── drone_before.mp4
    ├── drone_after.png
    ├── hand.png
    ├── av.png
    ├── stateful_agent.jpg
    └── favicon/           # Browser icons
        ├── favicon.ico
        ├── favicon.svg
        ├── favicon-96x96.png
        ├── apple-touch-icon.png
        └── site.webmanifest
```

---

## What's Included

### Content Sections
- ✅ Professional profile with photo
- ✅ News/updates section
- ✅ Entrepreneurial Experience (Intuition Core Inc.)
  - Clickable logo linking to company website
  - Embedded demo video
  - $950K funding details
- ✅ Research Section (5 projects)
  - LiDAR Semantic Segmentation (highlighted, NSF-funded)
  - Mesh & Texture Optimization (highlighted)
  - Flying in the Wild, No GPS
  - Hand Generation (Hi-Fi, submitted to FG2025)
  - Autonomous Driving Scene Reconstruction
- ✅ Education (2 institutions)
  - UC Berkeley (clickable logo)
  - Fudan University (clickable logo)
- ✅ Other Selected Projects
  - Stateful-Agent with GitHub links
- ✅ Skills & Technical Expertise
- ✅ Professional footer with attribution

### Features
- ✅ Interactive hover effects (3 projects)
- ✅ Autoplay videos with loop
- ✅ Mixed media (videos + images)
- ✅ Mobile-responsive design
- ✅ Custom favicon for all devices
- ✅ Hidden URLs (no naked links)
- ✅ Clickable logos linking to websites
- ✅ Paper links to Google Drive
- ✅ GitHub repository links
- ✅ Clean, academic aesthetic

---

## Performance Notes

### Large Files
Some media files are large:
- `lidar_after.mp4` (38M)
- `lidar_before.mp4` (22M)
- `hand.png` (11M)
- `av.png` (12M)
- `drone_before.mp4` (7.2M)

**Recommendations:**
1. **For GitHub Pages:** Works fine, but initial load may be slow
2. **To optimize:**
   - Compress PNG files to <2MB using tools like TinyPNG
   - Reduce video quality/size if needed
   - Consider using video hosting (YouTube, Vimeo) for very large files

**Current total size:** ~100MB

---

## Common Questions

### Q: Videos aren't playing
**A:**
- Use a local server (`python3 -m http.server 8000`)
- Check browser console for errors
- Ensure video format is MP4
- Some browsers block autoplay without user interaction

### Q: Hover effect not working
**A:**
- Make sure both files exist (`_before` and `_after`)
- Check file extensions match HTML (.mp4, .png, etc.)
- Clear browser cache

### Q: Page loads slowly
**A:**
- Large video files take time to load
- Consider compressing media files
- Videos load progressively, so page is usable while loading

### Q: How do I update content?
**A:**
- Edit `index.html` directly
- Follow the patterns in existing sections
- Test locally before deploying

### Q: Can I use a custom domain?
**A:** Yes! With GitHub Pages:
1. Deploy to GitHub Pages
2. Add `CNAME` file with your domain
3. Configure DNS A records with your domain provider

### Q: How do I add Google Analytics?
**A:** Add before `</head>` tag:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR_GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR_GA_ID');
</script>
```

---

## Next Steps

1. ✅ ~~Add all media files~~ **COMPLETE**
2. **Test locally** - Verify everything works
3. **Deploy to GitHub Pages** - Go live!
4. **Share your link** - Add to CV, email signature, LinkedIn
5. **Keep updated** - Add new projects and achievements

---

## Credits

Template from [Jon Barron](https://github.com/jonbarron/jonbarron_website).

---

## Pro Tips

1. **Test before deploying** - Check all links and videos work
2. **Mobile test** - View on phone to check responsive design
3. **Get feedback** - Ask colleagues to review
4. **Update regularly** - Keep content fresh
5. **Monitor analytics** - See what visitors find interesting
6. **Optimize images** - Compress large files for faster loading
7. **Use custom domain** - Looks more professional
8. **Share widely** - Add link everywhere relevant
9. **Keep backups** - Save copies of your site files
10. **Version control** - Use git to track changes

---

**Your homepage is ready to impress! 🚀**

**Last updated:** November 2025
