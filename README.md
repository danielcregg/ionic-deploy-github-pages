# Ionic GitHub Pages Deployment
[![Deploy Ionic App to GitHub Pages](https://github.com/danielcregg/ionic-deploy-github-pages/actions/workflows/deploy-to-gh-pages.yml/badge.svg)](https://github.com/danielcregg/ionic-deploy-github-pages/actions/workflows/deploy-to-gh-pages.yml)

Deploy your Ionic Angular app to GitHub Pages automatically using GitHub Actions.

## 🚀 Setup Instructions (2 Steps)

1. **Add the workflow file to your repo**:
   - Option A: Copy the above GitHub Workflow `.github/workflows/deploy-to-gh-pages.yml` to your Ionic Angular app repository.
   - Option B: Use curl in terminal:
     ```bash
     mkdir -p .github/workflows && \
     curl -o .github/workflows/deploy-to-gh-pages.yml https://raw.githubusercontent.com/danielcregg/ionic-deploy-github-pages/main/.github/workflows/deploy-to-gh-pages.yml
     ```

2. **Enable GitHub Pages**:
   - Go to repository **Settings** → **Pages**
   - Under "Build and deployment", select **GitHub Actions** as the source

That's it! Push your changes and your app will deploy to `https://<username>.github.io/<repo-name>/`

## ✨ Features

- 🔄 **Zero Config**: Works automatically with any Ionic Angular project
- 🎯 **Smart Detection**: Finds your project whether in root or subdirectory
- 🏃 **Fast Builds**: Implements intelligent caching for quick deployments
- 🔍 **Auto-Detection**:
  - Detects standalone vs NgModule projects
  - Identifies correct Node.js version from project
  - Determines correct production configuration
- 🛠️ **Built-in Optimizations**:
  - Parallel build processing
  - Efficient dependency caching
  - Optimized production builds

## 📋 Requirements

- A public GitHub repository (or GitHub Pro/Enterprise for private repos)
- An Ionic Angular project with:
  - `ionic.config.json`
  - `package.json`
  - `angular.json`

## 🤔 Common Questions

- **Q: Will this work with my Ionic version?**
  - A: Yes! The workflow automatically detects your project's configuration

- **Q: Where will my app be deployed?**
  - A: Your app will be available at `https://<username>.github.io/<repo-name>/`

- **Q: What if my app is in a subdirectory?**
  - A: The workflow automatically finds your Ionic project, regardless of location

## 🔍 Deployment Status

After pushing changes:
1. Go to your repository's **Actions** tab
2. Click on the latest workflow run
3. At the bottom of the logs, you'll find a clickable link to your deployed site

## 📝 License

MIT License - feel free to use in your own projects!
