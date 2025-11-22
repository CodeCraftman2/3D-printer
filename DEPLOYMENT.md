# GitHub Pages Deployment Guide

This guide will walk you through deploying this 3D printer project to GitHub Pages.

## Quick Start

Your repository is now ready for GitHub Pages deployment! Just follow these 3 simple steps:

### Step 1: Enable GitHub Pages

1. Go to your repository: https://github.com/CodeCraftman2/3D-printer
2. Click on **Settings** (top navigation bar)
3. In the left sidebar, click **Pages**
4. Under "Build and deployment":
   - For **Source**, select **GitHub Actions** from the dropdown
   
That's it! No need to select a branch or folder.

### Step 2: Trigger the Deployment

You have two options:

#### Option A: Push to Main Branch (Automatic)
```bash
# Make sure your changes are on the main branch
git checkout main
git merge copilot/deploy-github-pages
git push origin main
```

The workflow will automatically run and deploy your site.

#### Option B: Manual Trigger
1. Go to the **Actions** tab in your repository
2. Click on "Deploy to GitHub Pages" workflow (left sidebar)
3. Click the **Run workflow** button (top right)
4. Select the branch (usually `main`)
5. Click the green **Run workflow** button

### Step 3: Access Your Site

After the workflow completes (usually takes 1-2 minutes):

🌐 Your site will be live at: **https://codecraftman2.github.io/3D-printer/**

## Monitoring Deployment

### Check Deployment Status

1. **Actions Tab**: 
   - Go to the Actions tab to see all workflow runs
   - ✅ Green checkmark = successful deployment
   - ❌ Red X = failed deployment (check logs for details)

2. **Environments**:
   - Look for the **github-pages** environment in your repository
   - Shows the currently deployed version
   - Click "View deployment" to open your live site

### Troubleshooting

**Deployment Fails?**
- Check that GitHub Pages is enabled in Settings → Pages
- Ensure the Source is set to "GitHub Actions"
- Review the workflow logs in the Actions tab
- Make sure the repository is public (or you have GitHub Pro for private repos)

**404 Error on Site?**
- Verify the base path in `index.html` matches your repository name
- Current base path is `/3D-printer/` - should match repo name
- Wait a few minutes after deployment for DNS propagation

**Assets Not Loading?**
- Check the browser console for errors
- Verify all asset paths in `index.html` start with `/3D-printer/`
- Clear browser cache and try again

## Understanding the Setup

### What We Created

1. **GitHub Actions Workflow** (`.github/workflows/deploy.yml`):
   - Automatically deploys on push to `main` branch
   - Can be manually triggered
   - Uses official GitHub Pages actions
   - Handles all the deployment complexity for you

2. **Repository Configuration**:
   - Built static files already present (`index.html`, `assets/`)
   - Proper base path configured for GitHub Pages
   - No build step needed (pre-built with Vite)

### The Deployment Process

When triggered, the workflow:
1. ✅ Checks out your code
2. ✅ Configures GitHub Pages settings
3. ✅ Uploads all files as an artifact
4. ✅ Deploys to GitHub Pages
5. ✅ Your site goes live!

## Making Updates

To update your deployed site:

1. Make changes to your files
2. Commit and push to the `main` branch:
   ```bash
   git add .
   git commit -m "Update site"
   git push origin main
   ```
3. The workflow automatically runs and deploys the updates
4. Your site updates in 1-2 minutes

## Additional Resources

- [GitHub Pages Documentation](https://docs.github.com/pages)
- [GitHub Actions Documentation](https://docs.github.com/actions)
- [Vite Static Deploy Guide](https://vitejs.dev/guide/static-deploy.html)

## Need Help?

If you encounter issues:
1. Check the [Actions tab](https://github.com/CodeCraftman2/3D-printer/actions) for error logs
2. Review this guide's troubleshooting section
3. Ensure all prerequisites are met
4. Create an issue in the repository for support
