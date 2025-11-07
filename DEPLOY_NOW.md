# 🚀 Deploy to GitHub Pages NOW - Quick Guide

## Step-by-Step (5 Minutes)

### Step 1: Push to Main Branch

First, merge your changes to the main branch:

```bash
# Check current branch
git branch

# If you're on a feature branch, merge to main
git checkout main
git merge <your-feature-branch>
git push origin main
```

**OR** if you don't have a main branch yet:

```bash
# Rename current branch to main
git branch -M main
git push -u origin main
```

---

### Step 2: Enable GitHub Pages

1. **Go to your repository on GitHub:**
   ```
   https://github.com/lewbei/IJORAS-citation-convertor
   ```

2. **Click on "Settings" tab** (top right)

3. **Click on "Pages"** (left sidebar)

4. **Under "Build and deployment":**
   - **Source:** Select "GitHub Actions"
   - (The workflow file we created will automatically deploy)

5. **Click "Save"**

---

### Step 3: Trigger Deployment

The deployment will trigger automatically when you push to main. To trigger it now:

**Option A: Push to main** (if you did Step 1)
```bash
# Already done if you merged/pushed to main
```

**Option B: Manual trigger**
1. Go to "Actions" tab on GitHub
2. Click "Deploy to GitHub Pages" workflow
3. Click "Run workflow"
4. Click green "Run workflow" button

---

### Step 4: Wait for Deployment (1-2 minutes)

1. Go to **Actions** tab
2. You'll see a workflow running (yellow dot)
3. Wait for it to complete (green checkmark ✓)
4. Deployment complete!

---

### Step 5: Visit Your Live Site! 🎉

Your site will be available at:

```
https://lewbei.github.io/IJORAS-citation-convertor/
```

**Bookmark this URL!**

---

## Troubleshooting

### "Pages is not enabled"
- Make sure you selected "GitHub Actions" as source
- Make sure the repository is public (or you have GitHub Pro)

### "Deployment failed"
- Check the Actions tab for error messages
- Ensure all files are committed and pushed
- Try re-running the workflow

### "404 Not Found"
- Wait 2-3 minutes for DNS propagation
- Make sure index.html is in the root directory
- Clear browser cache and try again

### "Site loads but features don't work"
- Check browser console for errors
- Ensure you entered a valid Gemini API key
- Try in an incognito/private window

---

## Quick Verification Checklist

Once deployed, test these on the live site:

- [ ] ✅ Site loads at GitHub Pages URL
- [ ] ✅ Dark mode toggle works
- [ ] ✅ Can save API key
- [ ] ✅ Load example works
- [ ] ✅ Convert references works (with your API key)
- [ ] ✅ Copy to clipboard works
- [ ] ✅ Keyboard shortcuts work (try Ctrl/⌘ + Enter)
- [ ] ✅ Mobile responsive (check on phone)

---

## Updating Your Live Site

After the initial deployment, any push to main will auto-deploy:

```bash
# Make changes to your files
git add .
git commit -m "Your update message"
git push origin main

# Wait 1-2 minutes - site updates automatically!
```

---

## Custom Domain (Optional)

Want to use your own domain like `references.yourdomain.com`?

1. Add a CNAME file:
   ```bash
   echo "your-domain.com" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push origin main
   ```

2. Update DNS settings at your domain registrar:
   - Add CNAME record pointing to: `lewbei.github.io`

3. In GitHub Settings → Pages:
   - Enter your custom domain
   - Enable "Enforce HTTPS"

4. Wait 24-48 hours for DNS propagation

---

## Success! 🎉

Your IJORAS Citation Converter is now live on the internet!

**Share your live site:**
- Tweet about it
- Share with colleagues
- Add to your CV/portfolio
- Submit to academic tools directories

**Next steps:**
- Share the URL with potential users
- Get feedback
- Make improvements
- Keep the README updated

---

**Your Live URL:**
```
https://lewbei.github.io/IJORAS-citation-convertor/
```

**Test it now!** 🚀
