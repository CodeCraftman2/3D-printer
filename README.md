# 3D Printer Viewer

A 3D printer visualization built with Vite and deployed on GitHub Pages.

## 🚀 Deployment to GitHub Pages

This project is configured to automatically deploy to GitHub Pages. Follow these steps:

### Prerequisites
- Repository owner or admin access to the GitHub repository
- The repository should be public (or you need GitHub Pro/Team for private repo Pages)

### Setup Instructions

1. **Enable GitHub Pages in Repository Settings:**
   - Go to your repository on GitHub
   - Navigate to **Settings** → **Pages**
   - Under **Build and deployment**:
     - Set **Source** to "GitHub Actions"
   
2. **Deploy Your Site:**
   
   The site will automatically deploy when you:
   - Push to the `main` branch
   - Manually trigger the workflow from the Actions tab
   
3. **Manual Deployment (Optional):**
   - Go to the **Actions** tab in your GitHub repository
   - Select the "Deploy to GitHub Pages" workflow
   - Click **Run workflow** → **Run workflow**

### Access Your Site

Once deployed, your site will be available at:
```
https://codecraftman2.github.io/3D-printer/
```

### Deployment Status

You can check the deployment status:
- Go to the **Actions** tab to see workflow runs
- Look for the green checkmark ✓ indicating successful deployment
- Check the **Environments** section in the repository to see active deployments

## 🔧 Local Development

To work with the source code and rebuild the project, you would need to:
1. Clone the repository
2. Set up the development environment
3. Build the project with Vite
4. The built files are already included in this repository

## 📝 Notes

- The project is configured with base path `/3D-printer/` for GitHub Pages
- All assets are properly referenced relative to this base path
- The workflow uses GitHub Actions for automated deployment
