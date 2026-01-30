# ip.py Website

Website for the Infinite Particularity installation by blueOrange Design Research.

## Project Structure

```
ippy-website/
├── css/
│   └── style.css
├── images/           ← Create this folder for your images
├── videos/           ← Create this folder for your videos
├── index.html
├── algo.html
├── install.html
├── memory.html
├── particularity.html
├── render.html
└── gallery.html
```

---

## Adding Images

### 1. Create an `images` folder in your project

### 2. Add your images to the folder

### 3. Replace placeholders in HTML files

**Home page (index.html) - Hero images:**
```html
<!-- Change this: -->
<div class="hero-image-placeholder"></div>

<!-- To this: -->
<img src="images/your-image.jpg" alt="Description" class="hero-image">
```

**Install page (install.html) - Triptych:**
```html
<!-- Change this: -->
<div class="triptych-box"></div>

<!-- To this: -->
<img src="images/memory-screen.jpg" alt="Memory screen" class="triptych-image">
```

**Gallery page (gallery.html):**
```html
<!-- Change this: -->
<div class="gallery-item">PICTURES</div>

<!-- To this: -->
<img src="images/gallery1.jpg" alt="Gallery image" class="gallery-image">
```

---

## Adding GIFs

GIFs will loop automatically. Just add your GIF files to the `images` folder.

```html
<!-- Replace the video-placeholder div with: -->
<div class="gif-container">
    <img src="images/your-demo.gif" alt="Demo">
</div>
```

The GIF will automatically loop forever and fill the container.

**Tip:** If your GIFs are too large, you can convert videos to optimized GIFs using:
- [ezgif.com](https://ezgif.com/video-to-gif)
- [CloudConvert](https://cloudconvert.com/mp4-to-gif)
- FFmpeg: `ffmpeg -i video.mp4 -vf "fps=15,scale=800:-1" output.gif`

---

## Deploy to GitHub Pages

### Step 1: Create a GitHub repository

1. Go to [github.com](https://github.com) and sign in
2. Click the **+** icon → **New repository**
3. Name it `ippy-website` (or any name you want)
4. Keep it **Public**
5. Click **Create repository**

### Step 2: Upload your files

**Option A: Using GitHub web interface (easiest)**

1. In your new repo, click **"uploading an existing file"**
2. Drag and drop ALL your website files (index.html, algo.html, css folder, images folder, etc.)
3. Click **Commit changes**

**Option B: Using Git command line**

```bash
# Navigate to your website folder
cd ippy-website

# Initialize git
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit"

# Add your GitHub repo as remote (replace with your actual URL)
git remote add origin https://github.com/YOUR_USERNAME/ippy-website.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (tab at the top)
3. Scroll down to **Pages** (in the left sidebar)
4. Under **Source**, select **Deploy from a branch**
5. Under **Branch**, select **main** and **/ (root)**
6. Click **Save**

### Step 4: Access your site

After a few minutes, your site will be live at:

```
https://YOUR_USERNAME.github.io/ippy-website/
```

---

## Custom Domain (Optional)

If you want to use a custom domain like `infiniteparticularity.com`:

1. In your repo, create a file called `CNAME` (no extension)
2. Add your domain name to it: `infiniteparticularity.com`
3. In your domain registrar, add these DNS records:
   - A record: `185.199.108.153`
   - A record: `185.199.109.153`
   - A record: `185.199.110.153`
   - A record: `185.199.111.153`
   - CNAME record: `www` → `YOUR_USERNAME.github.io`

---

## Troubleshooting

**Images not showing?**
- Make sure file paths are correct (case-sensitive!)
- Check that images are in the `images` folder
- Use relative paths: `images/photo.jpg` not `/images/photo.jpg`

**CSS not loading?**
- Verify the css folder is uploaded
- Check the link in HTML: `<link rel="stylesheet" href="css/style.css">`

**GitHub Pages not updating?**
- Changes can take 1-5 minutes to appear
- Try hard refresh: `Ctrl+Shift+R` (Windows) or `Cmd+Shift+R` (Mac)
- Check the Actions tab in your repo for deployment status
