# My Study Notes Blog

A clean, minimal static blog hosted on GitHub Pages.

## File structure

```
/
├── index.html        ← homepage (post list)
├── style.css         ← all styles
├── about.html        ← about page
└── posts/
    ├── hardy-weinberg.html    ← sample post
    ├── historiography.html    ← (placeholder)
    └── trolley-problem.html   ← (placeholder)
```

## How to deploy to GitHub Pages (step by step)

### 1. Create a GitHub account
If you don't have one, go to https://github.com and sign up.

### 2. Create a new repository
- Go to https://github.com/new
- Name it exactly: `yourusername.github.io`  
  (replace `yourusername` with your actual GitHub username)
- Set it to **Public**
- Click **Create repository**

### 3. Upload your files
**Option A — via GitHub web interface (easiest):**
- Open your new repository
- Click **Add file → Upload files**
- Drag and drop ALL the files from this folder
- Make sure to upload the `posts/` folder too (GitHub will let you drag folders)
- Click **Commit changes**

**Option B — via Git (if you have it installed):**
```bash
git init
git add .
git commit -m "Initial blog setup"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

### 4. Enable GitHub Pages
- Go to your repository → **Settings** → **Pages** (in the left sidebar)
- Under **Source**, select **Deploy from a branch**
- Select branch: `main`, folder: `/ (root)`
- Click **Save**

### 5. Visit your blog
After ~1–2 minutes, your blog will be live at:
**https://yourusername.github.io**

---

## How to add a new post

1. Duplicate the file `posts/hardy-weinberg.html`
2. Rename it to something descriptive, e.g. `posts/my-new-topic.html`
3. Edit the content inside (title, date, tags, body text)
4. Open `index.html` and add a new `<article class="post-card">` block for the post
5. Push/upload to GitHub — it'll go live in seconds

## Customizing your blog

- **Your name:** search for `[Your Name]` and replace it everywhere
- **Tags:** update the tag buttons in `index.html` and the `data-tags` attribute on each post card
- **Colors:** edit the `:root` variables at the top of `style.css`
- **Intro text:** edit the `.page-intro` section in `index.html`
