# Deployment Instructions for GitHub Pages

## Quick Deployment Guide

These files are ready to deploy to your GitHub Pages repository: **prajjwalsilwal.github.io**

### Files to Deploy:
- `index.html` - Main website file
- `style.css` - Stylesheet
- `Prajjwal_Silwal_Resume.pdf` - Your resume (should already be in the repo)

## Step-by-Step Instructions

### Option 1: Upload via GitHub Web Interface

1. **Go to your repository**: https://github.com/prajjwalsilwal/prajjwalsilwal.github.io

2. **Upload files**:
   - Click "Add file" → "Upload files"
   - Drag and drop `index.html` and `style.css`
   - (Or replace existing files if they exist)

3. **Commit changes**:
   - Add a commit message: "Update portfolio website UI"
   - Click "Commit changes"

4. **Verify GitHub Pages is enabled**:
   - Go to Settings → Pages
   - Source should be set to "Deploy from a branch"
   - Branch should be `main` (or `master`)
   - Save

5. **View your site**: 
   - Wait 1-2 minutes for deployment
   - Visit: https://prajjwalsilwal.github.io

### Option 2: Deploy via Git (Command Line)

```bash
# Navigate to your GitHub Pages repo directory
cd path/to/prajjwalsilwal.github.io

# Copy files from this directory
cp path/to/portfolio/website/index.html .
cp path/to/portfolio/website/style.css .

# Commit and push
git add index.html style.css
git commit -m "Update portfolio website UI"
git push origin main
```

### Option 3: Copy Files Directly

1. Open the `website` folder in this portfolio directory
2. Copy `index.html` and `style.css`
3. Paste them into your `prajjwalsilwal.github.io` repository folder
4. Commit and push to GitHub

## Customization Tips

### Update Resume Link
If your resume filename is different, update line 42 in `index.html`:
```html
<a href="YOUR_RESUME_FILENAME.pdf" class="btn btn-secondary" download>
```

### Verify Links
The website links to:
- Portfolio repository: `https://github.com/prajjwalsilwal/portfolio`
- LinkedIn: `https://linkedin.com/in/prajjwal-silwal`
- GitHub: `https://github.com/prajjwalsilwal`

Make sure these are correct!

### Add Custom Domain (Optional)
If you have a custom domain:
1. Add a `CNAME` file in your repo with your domain name
2. Update DNS settings with your domain provider
3. Configure in GitHub Pages settings

## Testing Locally

Before deploying, test locally:

```bash
# Using Python
python -m http.server 8000

# Using Node.js (if installed)
npx http-server

# Then visit http://localhost:8000
```

## Features Included

✅ Responsive design (mobile-friendly)
✅ Smooth scrolling navigation
✅ Interactive project cards
✅ Contact section with social links
✅ Professional gradient hero section
✅ Animated sections on scroll
✅ Mobile hamburger menu

## Troubleshooting

**Site not updating?**
- Wait 1-2 minutes after pushing
- Check GitHub Actions tab for deployment status
- Hard refresh browser (Ctrl+F5 or Cmd+Shift+R)

**Styles not loading?**
- Verify `style.css` is in the same directory as `index.html`
- Check file paths are correct
- Clear browser cache

**Mobile menu not working?**
- Make sure JavaScript is enabled in browser
- Check browser console for errors

## Next Steps

After deployment:
1. ✅ Share your website URL on LinkedIn
2. ✅ Add to your resume
3. ✅ Include in job applications
4. ✅ Update as you complete new projects

Your website will be live at: **https://prajjwalsilwal.github.io**

