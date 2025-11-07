# Deployment Guide

This guide explains how to deploy the IJORAS Citation Converter to various hosting platforms.

## Table of Contents

- [GitHub Pages](#github-pages)
- [Netlify](#netlify)
- [Vercel](#vercel)
- [Local Hosting](#local-hosting)
- [Custom Domain](#custom-domain)

---

## GitHub Pages

GitHub Pages is the easiest and free way to deploy this project.

### Method 1: Automatic Deployment (Recommended)

1. **Fork or clone the repository**
   ```bash
   git clone https://github.com/lewbei/IJORAS-citation-convertor.git
   cd IJORAS-citation-convertor
   ```

2. **Push to your GitHub repository**
   ```bash
   git remote set-url origin https://github.com/YOUR_USERNAME/IJORAS-citation-convertor.git
   git push origin main
   ```

3. **Enable GitHub Pages**
   - Go to your repository on GitHub
   - Click **Settings** → **Pages**
   - Under **Source**, select **main** branch
   - Select **/ (root)** folder
   - Click **Save**

4. **Access your site**
   - Your site will be available at: `https://YOUR_USERNAME.github.io/IJORAS-citation-convertor/`
   - It may take a few minutes to deploy

### Method 2: Using gh-pages Branch

1. **Create gh-pages branch**
   ```bash
   git checkout -b gh-pages
   git push origin gh-pages
   ```

2. **Enable GitHub Pages**
   - Go to Settings → Pages
   - Select **gh-pages** branch
   - Click Save

### Updating Your Deployment

Simply push changes to your main branch (or gh-pages if you chose that method):

```bash
git add .
git commit -m "Update site"
git push origin main
```

GitHub Pages will automatically rebuild and deploy your site.

---

## Netlify

Netlify offers continuous deployment and is very easy to set up.

### Deploy to Netlify

1. **Sign up at [Netlify](https://www.netlify.com/)**

2. **Connect your repository**
   - Click "New site from Git"
   - Choose GitHub and authorize
   - Select your repository

3. **Configure build settings**
   - **Build command:** (leave empty - it's a static HTML site)
   - **Publish directory:** `.` (root directory)
   - Click "Deploy site"

4. **Access your site**
   - You'll get a URL like: `https://random-name-12345.netlify.app`
   - You can customize this in Site settings

### Netlify Benefits

- Automatic HTTPS
- Custom domains
- Continuous deployment
- Instant rollbacks
- Free tier available

### Netlify Configuration (Optional)

Create a `netlify.toml` file:

```toml
[build]
  publish = "."

[[headers]]
  for = "/*"
  [headers.values]
    X-Frame-Options = "DENY"
    X-Content-Type-Options = "nosniff"
    X-XSS-Protection = "1; mode=block"
```

---

## Vercel

Vercel is another excellent option for static sites.

### Deploy to Vercel

1. **Sign up at [Vercel](https://vercel.com/)**

2. **Import your repository**
   - Click "New Project"
   - Import from GitHub
   - Select your repository

3. **Configure project**
   - **Framework Preset:** Other
   - **Root Directory:** `./`
   - **Build Command:** (leave empty)
   - **Output Directory:** `./`
   - Click "Deploy"

4. **Access your site**
   - You'll get a URL like: `https://your-project.vercel.app`

### Vercel Benefits

- Extremely fast CDN
- Automatic HTTPS
- Preview deployments for PRs
- Custom domains
- Free tier for personal projects

### Vercel Configuration (Optional)

Create a `vercel.json` file:

```json
{
  "version": 2,
  "public": true,
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        {
          "key": "X-Content-Type-Options",
          "value": "nosniff"
        },
        {
          "key": "X-Frame-Options",
          "value": "DENY"
        }
      ]
    }
  ]
}
```

---

## Local Hosting

For testing or internal use, you can host locally.

### Python Simple Server

```bash
cd IJORAS-citation-convertor

# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

Access at: `http://localhost:8000`

### Node.js http-server

```bash
npm install -g http-server
cd IJORAS-citation-convertor
http-server -p 8000
```

Access at: `http://localhost:8000`

### PHP Built-in Server

```bash
cd IJORAS-citation-convertor
php -S localhost:8000
```

Access at: `http://localhost:8000`

---

## Custom Domain

### GitHub Pages + Custom Domain

1. **Add CNAME file**
   ```bash
   echo "yourdomain.com" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

2. **Configure DNS**

   For apex domain (example.com):
   ```
   A Record: 185.199.108.153
   A Record: 185.199.109.153
   A Record: 185.199.110.153
   A Record: 185.199.111.153
   ```

   For subdomain (www.example.com):
   ```
   CNAME: YOUR_USERNAME.github.io
   ```

3. **Enable in GitHub**
   - Settings → Pages → Custom domain
   - Enter your domain
   - Enable "Enforce HTTPS"

### Netlify + Custom Domain

1. **Go to Domain settings**
   - Click "Add custom domain"
   - Enter your domain

2. **Configure DNS**
   - Follow Netlify's instructions
   - Usually involves adding a CNAME record

3. **HTTPS**
   - Netlify automatically provisions SSL certificates

### Vercel + Custom Domain

1. **Go to Project Settings → Domains**
   - Add your domain

2. **Configure DNS**
   - Add CNAME record pointing to `cname.vercel-dns.com`

3. **HTTPS**
   - Automatic with Let's Encrypt

---

## Deployment Checklist

Before deploying to production:

- ✅ Test all features thoroughly
- ✅ Check responsive design on mobile
- ✅ Test in multiple browsers
- ✅ Verify dark mode works
- ✅ Ensure no console errors
- ✅ Remove any test API keys
- ✅ Update README with live URL
- ✅ Add proper meta tags for SEO
- ✅ Test keyboard shortcuts
- ✅ Verify all links work

---

## Environment Variables

This project doesn't use server-side environment variables since it's a static site. API keys are stored in the user's browser localStorage.

**Security Note:** Users must provide their own Gemini API keys, which are stored locally and never exposed in the codebase.

---

## Continuous Integration / Deployment

### GitHub Actions (Optional)

Create `.github/workflows/deploy.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./
```

---

## Troubleshooting

### GitHub Pages not updating

1. Check GitHub Actions tab for build errors
2. Clear browser cache
3. Wait a few minutes (can take 5-10 minutes)
4. Verify correct branch is selected in Settings

### 404 errors

1. Ensure `index.html` is in the root directory
2. Check branch and folder settings
3. Verify repository is public (or you have GitHub Pro for private repos)

### HTTPS not working

1. Enable "Enforce HTTPS" in GitHub Pages settings
2. Wait for certificate provisioning (can take 24 hours)
3. Clear DNS cache

### Custom domain not working

1. Verify DNS propagation (use tools like `dig` or whatsmydns.net)
2. Check CNAME file exists and has correct domain
3. Wait for DNS propagation (can take 24-48 hours)

---

## Performance Optimization

For better performance after deployment:

1. **Enable CDN** (automatic with GitHub Pages, Netlify, Vercel)
2. **Minify assets** (optional for this small project)
3. **Enable caching** headers
4. **Use compression** (automatic with most hosts)

---

## Monitoring

### Google Analytics (Optional)

Add to `<head>` in index.html:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR_GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR_GA_ID');
</script>
```

---

## Support

If you encounter deployment issues:

1. Check the hosting platform's documentation
2. Open an issue on GitHub
3. Check existing issues for solutions

---

## Next Steps

After deployment:

1. Test the live site thoroughly
2. Share the URL with users
3. Monitor for issues
4. Set up analytics (optional)
5. Configure custom domain (optional)

---

**Recommended Deployment:** GitHub Pages (easiest) or Netlify (most features)

For most users, GitHub Pages is the best choice as it's free, easy to set up, and integrates perfectly with your repository.
