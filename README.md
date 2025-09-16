# Blubox Guide Viewer

This is the public viewer for Blubox guides.

## Quick Setup for GitHub Pages

1. Create a new GitHub repository named `blubox-viewer` (or any name you prefer)

2. Push this folder to GitHub:
```bash
cd github-pages-viewer
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/blubox-viewer.git
git push -u origin main
```

3. Enable GitHub Pages:
   - Go to your repository Settings
   - Scroll to "Pages" section
   - Under "Source", select "Deploy from a branch"
   - Select "main" branch and "/ (root)" folder
   - Click Save

4. Your viewer will be available at:
   `https://YOUR_USERNAME.github.io/blubox-viewer/`

5. Update your extension to use this URL:
   - Edit `/extension/src/lib/supabase.ts`
   - Replace `http://localhost:8080` with your GitHub Pages URL
   - Rebuild the extension

## How It Works

- Guides are stored in Supabase
- This viewer fetches and displays them
- URLs look like: `https://YOUR_USERNAME.github.io/blubox-viewer/#/guide/YOUR-GUIDE-SLUG`
- The 404.html handles routing for direct guide links