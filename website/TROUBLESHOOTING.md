# GitHub Pages Troubleshooting Guide

## Your Site URLs

- **Repository**: https://github.com/prajjwalsilwal/prajjwalsilwal.github.io
- **Live Site**: https://prajjwalsilwal.github.io (this is where your website should appear)

## Common Issues & Solutions

### Issue 1: "404 Page Not Found" or Blank Page

**Solution**: Enable GitHub Pages

1. Go to your repository: https://github.com/prajjwalsilwal/prajjwalsilwal.github.io
2. Click **Settings** (top right of repository page)
3. Scroll down to **Pages** in the left sidebar
4. Under **Source**, select:
   - **Branch**: `main` (or `master` if that's your default)
   - **Folder**: `/ (root)`
5. Click **Save**
6. Wait 1-5 minutes for deployment

### Issue 2: Site Shows Repository Files Instead of Website

**Solution**: Make sure `index.html` is at the root of your repository

Your repository structure should look like:
```
prajjwalsilwal.github.io/
├── index.html        ← Must be here
├── style.css         ← Must be here
├── Prajjwal_Silwal_Resume.pdf
└── README.md
```

### Issue 3: Styles Not Loading

**Solution**: Check file paths

- `style.css` must be in the same directory as `index.html`
- The link in `index.html` should be: `<link rel="stylesheet" href="style.css">`
- Case-sensitive: Make sure it's `style.css` not `Style.css`

### Issue 4: Changes Not Appearing

**Solution**: Clear cache and wait

1. **Hard refresh** your browser:
   - Windows/Linux: `Ctrl + Shift + R` or `Ctrl + F5`
   - Mac: `Cmd + Shift + R`

2. **Wait**: GitHub Pages can take 1-5 minutes to update

3. **Check deployment status**:
   - Go to repository → **Actions** tab
   - Look for "pages build and deployment" workflow

### Issue 5: Site Still Not Working After Deployment

**Check These:**

1. **Verify files are committed**:
   - Go to your repository → **Code** tab
   - Make sure `index.html` and `style.css` are visible
   - Check if they were recently committed

2. **Check for errors in Actions**:
   - Repository → **Actions** tab
   - Look for any failed workflows (red X)
   - Click on failed workflow to see error details

3. **Test locally**:
   - Download your repository
   - Open `index.html` in a browser
   - Check browser console (F12) for errors

## Step-by-Step Fix

### If your site is completely broken:

1. **Verify GitHub Pages is enabled**:
   ```
   Repository → Settings → Pages
   Source: Deploy from a branch
   Branch: main / (root)
   Save
   ```

2. **Check your files are correct**:
   - Open `index.html` in your repository
   - Verify `style.css` link is correct: `<link rel="stylesheet" href="style.css">`
   - Make sure both files are in the root directory

3. **Force a redeploy**:
   - Make a small change to `index.html` (add a space)
   - Commit and push
   - This triggers a new deployment

4. **Wait and test**:
   - Wait 2-5 minutes
   - Visit: https://prajjwalsilwal.github.io
   - Try in incognito/private window

## Quick Checklist

- [ ] GitHub Pages is enabled in Settings → Pages
- [ ] Branch selected is `main` (or `master`)
- [ ] `index.html` is in the root directory
- [ ] `style.css` is in the root directory
- [ ] Files are committed and pushed
- [ ] Waited at least 2 minutes after enabling
- [ ] Tried hard refresh (Ctrl+Shift+R)
- [ ] Checked Actions tab for errors

## Still Not Working?

1. **Check Actions tab**:
   - Go to: https://github.com/prajjwalsilwal/prajjwalsilwal.github.io/actions
   - Look for any failed deployments

2. **Check file contents**:
   - Open `index.html` in GitHub
   - Make sure it's valid HTML (not corrupted)

3. **Try accessing via HTTPS**:
   - Make sure you're using: `https://prajjwalsilwal.github.io`
   - Not: `http://prajjwalsilwal.github.io` (without S)

4. **Check repository visibility**:
   - Make sure repository is **Public** (or you have GitHub Pro/Teams)

## Expected Result

After enabling GitHub Pages, your site should:
- Be accessible at: https://prajjwalsilwal.github.io
- Show your portfolio website (not a 404)
- Display styles correctly
- All links and buttons work

## Testing Locally

Before pushing to GitHub, test locally:

```bash
# Download your repo
git clone https://github.com/prajjwalsilwal/prajjwalsilwal.github.io.git
cd prajjwalsilwal.github.io

# Start a local server
python -m http.server 8000

# Open browser: http://localhost:8000
```

If it works locally but not on GitHub Pages, the issue is with GitHub Pages configuration.

