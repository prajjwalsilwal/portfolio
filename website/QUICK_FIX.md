# Quick Fix for GitHub Pages

## Most Common Issue: GitHub Pages Not Enabled

### Step 1: Enable GitHub Pages (CRITICAL)

1. **Go to your repository**: https://github.com/prajjwalsilwal/prajjwalsilwal.github.io

2. **Click "Settings"** (top right, next to "Insights")

3. **Click "Pages"** in the left sidebar

4. **Under "Source"**, select:
   - **Branch**: `main` 
   - **Folder**: `/ (root)`

5. **Click "Save"**

6. **Wait 1-5 minutes** for GitHub to deploy

7. **Visit**: https://prajjwalsilwal.github.io

---

## Step 2: Verify Files Are Correct

Your repository should have these files in the **root**:

- ✅ `index.html`
- ✅ `style.css`
- ✅ `Prajjwal_Silwal_Resume.pdf` (or update the name in HTML)

**Important**: If your resume filename is different, update line 42 in `index.html`:
```html
<!-- Change this if your resume has a different name -->
<a href="YOUR_RESUME_FILENAME.pdf" class="btn btn-secondary" download>
```

---

## Step 3: Check Deployment Status

1. Go to: https://github.com/prajjwalsilwal/prajjwalsilwal.github.io/actions

2. Look for "pages build and deployment" workflow

3. It should show a green checkmark ✅ if successful

4. If there's a red X ❌, click on it to see the error

---

## Step 4: Force Refresh

After enabling GitHub Pages:

1. Wait 2-5 minutes
2. **Hard refresh your browser**:
   - Windows/Linux: `Ctrl + Shift + R` or `Ctrl + F5`
   - Mac: `Cmd + Shift + R`
3. Try in **incognito/private window**

---

## Your Site URL

- ✅ **Correct**: https://prajjwalsilwal.github.io
- ❌ **Wrong**: https://github.com/prajjwalsilwal/prajjwalsilwal.github.io (this is the repo, not the site)

---

## If Still Not Working

### Check Actions Tab

1. Go to: https://github.com/prajjwalsilwal/prajjwalsilwal.github.io/actions
2. Look for failed deployments
3. Share the error message if you see one

### Check File Structure

Make sure `index.html` and `style.css` are in the root directory, not in a subfolder.

### Verify Resume File Name

The HTML references `Prajjwal_Silwal_Resume.pdf`. If your file is named differently:
- `Prajjwal_Silwal_Resume.docx` → Update HTML or rename file
- `resume.pdf` → Update HTML or rename file

---

## Quick Test

Visit this URL directly to see if GitHub Pages is working:
https://prajjwalsilwal.github.io/index.html

If this works but the root doesn't, it's a configuration issue.
If this doesn't work, GitHub Pages isn't enabled yet.

