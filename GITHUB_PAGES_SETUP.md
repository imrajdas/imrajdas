# GitHub Pages Deployment - Quick Setup

## Step 1: Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `portfolio` (or `rajdas.in`)
3. Make it **Public** (required for free GitHub Pages)
4. **Don't** initialize with README (we already have code)
5. Click "Create repository"

## Step 2: Push Your Code

Run these commands from the project directory:

```bash
cd /Users/rajdas/imrajdas

# Add GitHub as remote (replace 'imrajdas' with your username if different)
git remote add origin https://github.com/imrajdas/imrajdas.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. Click **Pages** (left sidebar)
4. Under "Build and deployment":
   - Source: Select **GitHub Actions**
5. That's it! The workflow will automatically run

## Step 4: Wait for Deployment

- Go to **Actions** tab in your repository
- You'll see the "Deploy Hugo site to GitHub Pages" workflow running
- Wait 1-2 minutes for it to complete
- Your site will be live at: `https://imrajdas.github.io/imrajdas/`

## Step 5: Custom Domain (Optional)

To use `rajdas.in`:

1. In GitHub Pages settings, add custom domain: `rajdas.in`
2. In your domain registrar (Namecheap, Cloudflare, etc.), add DNS records:
   ```
   Type: A
   Name: @
   Value: 185.199.108.153
   
   Type: A
   Name: @
   Value: 185.199.109.153
   
   Type: A
   Name: @
   Value: 185.199.110.153
   
   Type: A
   Name: @
   Value: 185.199.111.153
   
   Type: CNAME
   Name: www
   Value: imrajdas.github.io
   ```
3. Wait for DNS propagation (5 mins - 48 hours)
4. Enable "Enforce HTTPS" in GitHub Pages settings

## Troubleshooting

**If deployment fails:**
- Check the Actions tab for error messages
- Ensure repository is public
- Verify GitHub Pages is enabled with "GitHub Actions" as source

**If site doesn't load:**
- Wait a few minutes after first deployment
- Clear browser cache
- Check the Actions tab to ensure deployment succeeded

## Future Updates

Every time you push to the `main` branch, your site will automatically rebuild and deploy!

```bash
# Make changes to your content
# Then commit and push:
git add .
git commit -m "Update content"
git push
```

Your site will update automatically in 1-2 minutes! 🚀
