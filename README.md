# Ionic GitHub Pages Deployment

[![Deploy Ionic App to GitHub Pages](https://github.com/danielcregg/ionic-deploy-github-pages/actions/workflows/deploy.yml/badge.svg)](https://github.com/danielcregg/ionic-deploy-github-pages/actions/workflows/deploy.yml)

Deploy your Ionic Angular app to GitHub Pages automatically using GitHub Actions.

## 🚀 Setup Instructions

1. **Add the workflow file to your repo**:
- Copy the above GitHub workflow (.github/workflows/deploy.yml) to your Ionic Angular App repository
- You could use the below command if you are in a terminal:
 ```bash
   curl -o .github/workflows/deploy.yml https://raw.githubusercontent.com/danielcregg/ionic-deploy-github-pages/main/.github/workflows/deploy.yml
   ```
2. **Enable GitHub Pages**:
   - Go to repository **Settings** → **Pages**
   - Set Source to **GitHub Actions**

That's it! Push your changes and your app will deploy to `https://<username>.github.io/<repo-name>/`

## ✨ Features

- 🔄 **Zero Config**: Works automatically with any Ionic Angular project
- 🎯 **Smart Detection**: Finds your project whether in root or subdirectory
- 🏃 **Fast Builds**: Implements intelligent caching for quick deployments
