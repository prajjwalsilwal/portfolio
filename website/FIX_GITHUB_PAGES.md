# Fix GitHub Pages - Step by Step

## Problem Diagnosis

Based on your repository at https://github.com/prajjwalsilwal/prajjwalsilwal.github.io, the most likely issue is:

**GitHub Pages is not enabled or not configured correctly.**

## Solution: Enable GitHub Pages (5 Minutes)

### Step 1: Open Repository Settings

1. Go to: https://github.com/prajjwalsilwal/prajjwalsilwal.github.io
2. Click the **"Settings"** tab (top right of the repository)
   - It's next to "Insights", "Security", etc.

### Step 2: Navigate to Pages Section

1. In the left sidebar, scroll down and click **"Pages"**
   - It's under "Code and automation" section

### Step 3: Configure Source

Under **"Source"**, you'll see a dropdown:

1. **Select branch**: Choose `main` (or `master` if that's your default branch)
2. **Select folder**: Choose `/ (root)`
3. Click **"Save"**

### Step 4: Wait for Deployment

1. After clicking Save, you'll see a message like:
   ```
   Your site is published at https://prajjwalsilwal.github.io
   ```

2. **Wait 1-5 minutes** for GitHub to build and deploy your site

3. The build status will appear above the source selection

### Step 5: Verify It's Working

1. Visit: https://prajjwalsilwal.github.io
2. You should see your portfolio website!
3. If you see a 404, wait a few more minutes and try again

---

## What You Should See After Enabling

### In Settings → Pages:

- ✅ Green checkmark: "Your site is published at..."
- ✅ Recent deployment with status "completed"
- ✅ Source set to: `main` branch, `/ (root)` folder

### On Your Site (https://prajjwalsilwal.github.io):

- ✅ Hero section with gradient background
- ✅ Navigation menu
- ✅ Your name and title
- ✅ All sections (About, Projects, Skills, etc.)

---

## Common Issues After Enabling

### Issue: Still see 404 after 5 minutes

**Fix:**
1. Check **Actions** tab for build errors
2. Verify `index.html` is in the root directory
3. Hard refresh browser (Ctrl+Shift+R)
4. Try incognito window

### Issue: Styles not loading (site looks broken)

**Fix:**
1. Verify `style.css` is in the root directory
2. Check `index.html` line 8 has: `<link rel="stylesheet" href="style.css">`
3. Hard refresh browser (Ctrl+Shift+R)

### Issue: Resume download doesn't work

**Fix:**
1. Check if resume file exists in repository
2. Verify filename matches exactly in `index.html` line 42
3. Current reference: `Prajjwal_Silwal_Resume.pdf`
   - If your file is `Prajjwal_Silwal_Resume.docx`, update the HTML or rename the file

---

## Verification Checklist

After enabling GitHub Pages, verify:

- [ ] Settings → Pages shows "Your site is published at..."
- [ ] Actions tab shows successful "pages build and deployment"
- [ ] https://prajjwalsilwal.github.io loads (not 404)
- [ ] Website displays correctly with styles
- [ ] Navigation links work
- [ ] All sections are visible

---

## If GitHub Pages Still Doesn't Work

### Check Actions Tab

1. Go to: https://github.com/prajjwalsilwal/prajjwalsilwal.github.io/actions
2. Look for "pages build and deployment" workflow
3. If there's a red ❌, click it to see the error
4. Common errors:
   - Missing `index.html` in root
   - Syntax errors in HTML/CSS
   - Build timeout

### Force a New Deployment

1. Make a small change to `index.html` (add a comment or space)
2. Commit and push
3. This triggers a new deployment

### Check Repository Visibility

GitHub Pages works best with:
- ✅ Public repositories (free)
- ✅ Private repositories with GitHub Pro/Teams

---

## Need More Help?

1. **Check GitHub Status**: https://www.githubstatus.com/
2. **GitHub Docs**: https://docs.github.com/en/pages
3. **Community**: Check GitHub Community Discussions

---

## Quick Command Line Fix (If You Prefer Git)

```bash
# Clone your repository
git clone https://github.com/prajjwalsilwal/prajjwalsilwal.github.io.git
cd prajjwalsilwal.github.io

# Make a small change to trigger deployment
echo "<!-- Updated -->" >> index.html

# Commit and push
git add .
git commit -m "Trigger GitHub Pages deployment"
git push origin main

# Then enable GitHub Pages in Settings (still need to do this once)
```

After this, go to Settings → Pages and configure as described above.

