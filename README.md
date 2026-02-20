# Ionic Deploy GitHub Pages

![Ionic](https://img.shields.io/badge/Ionic-3880FF?style=flat-square&logo=ionic&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)

[![Deploy Ionic App to GitHub Pages](https://github.com/danielcregg/ionic-deploy-github-pages/actions/workflows/deploy-to-gh-pages-caller.yml/badge.svg)](https://github.com/danielcregg/ionic-deploy-github-pages/actions/workflows/deploy-to-gh-pages-caller.yml)

Deploy any Ionic Angular app to GitHub Pages automatically with a single reusable GitHub Actions workflow. Zero configuration required.

**Live Demo:** [https://danielcregg.github.io/ionic-deploy-github-pages/](https://danielcregg.github.io/ionic-deploy-github-pages/)

## Overview

This repository provides a reusable GitHub Actions workflow that automatically builds and deploys any Ionic Angular application to GitHub Pages. The workflow intelligently detects your project structure, Node.js version requirements, Angular configuration (standalone vs NgModule), and production build settings -- all without any manual configuration. It uses a caller/reusable workflow pattern so updates to the deployment logic are automatically inherited by all consuming repositories.

## Features

- **Zero Config** -- Works automatically with any Ionic Angular project
- **Smart Detection** -- Auto-detects project directory, Node.js version, standalone vs NgModule, and production config
- **Reusable Workflow** -- Caller/reusable pattern ensures consuming repos always get the latest deployment improvements
- **Optimized Builds** -- Parallel processing, AOT compilation, build optimizer, and dependency caching
- **SPA Routing** -- Automatically sets up 404.html fallback for client-side routing support
- **Build Verification** -- Validates build output before deployment with detailed error reporting
- **Flexible Structure** -- Finds your Ionic project whether in root or any subdirectory

## Prerequisites

- A GitHub repository containing an Ionic Angular project
- The project must include `ionic.config.json`, `package.json`, and `angular.json`
- A public repository (or GitHub Pro/Enterprise for private repos)

## Getting Started

### Installation

Add the caller workflow file to your Ionic Angular repository:

```bash
mkdir -p .github/workflows && \
curl -o .github/workflows/deploy-to-gh-pages-caller.yml \
  https://raw.githubusercontent.com/danielcregg/ionic-deploy-github-pages/main/.github/workflows/deploy-to-gh-pages-caller.yml
```

You only need the caller workflow file. The reusable workflow is referenced remotely and will always pull the latest version automatically.

### Usage

1. Enable GitHub Pages in your repository:
   - Go to **Settings** > **Pages**
   - Under **Build and deployment**, select **GitHub Actions** as the source

2. Commit and push the workflow file:
   ```bash
   git add .github/workflows/deploy-to-gh-pages-caller.yml
   git commit -m "ci: add GitHub Pages deployment workflow"
   git push
   ```

3. Your app will automatically deploy to:
   ```
   https://<your-username>.github.io/<repo-name>/
   ```

4. Monitor deployment status in the **Actions** tab of your repository.

## Tech Stack

- **Framework:** Ionic 8 with Angular 18 (standalone)
- **Language:** TypeScript
- **CI/CD:** GitHub Actions (reusable workflow)
- **Hosting:** GitHub Pages

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
