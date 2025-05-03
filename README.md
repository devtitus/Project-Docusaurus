# Project Docusaurus 📘

> 🚀 My personal documentation ecosystem built with [Docusaurus v3](https://docusaurus.io)

This repository contains all my technical notes, project documentation, system architecture diagrams, and learning logs — everything organized in one place using [Docusaurus](https://docusaurus.io), a modern static site generator made by Meta.

---

## 📌 Features

- ✅ Markdown-based documentation
- 🌗 Dark mode support
- 📱 Fully responsive design
- 🔍 Local search support _(optional plugin)_
- 🧩 Auto-generated sidebar navigation
- 🚀 Built for deployment on Netlify / GitHub Pages
- 🛠️ Easy to extend and customize

---

## 🛠️ Getting Started

### 1. Install dependencies

```bash
npm install
```

2. Start local development server

```bash
npm run start
```

This starts the dev server and opens the site in your browser. Most changes are reflected live.

3. Build for production

```bash
npm run build
```

The output will be in the build/ folder — ready to deploy.

🚀 Deployment
To deploy to GitHub Pages:

```bash
# If you're using SSH
USE_SSH=true npm run deploy
```

# Or if you're using HTTPS

GIT_USER=<Your-GitHub-Username> npm run deploy
This builds and pushes the site to the gh-pages branch automatically.

📁 Folder Structure

project-docusaurus/
├── docs/
│ └── All markdown documentation
├── src/
│ └── Custom React components/pages
├── static/
│ └── Images, PDFs, and other assets
├── docusaurus.config.js
│ └── Site configuration
├── sidebars.js
│ └── Sidebar navigation config
└── package.json
Built with ❤️ by Melwyn
