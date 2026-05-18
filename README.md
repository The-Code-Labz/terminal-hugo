# 🧠 NeuroClaw — Wiki & Blog

> **The official knowledge hub for the NeuroClaw AI ecosystem.**  
> Built with [Hugo](https://gohugo.io/) + the [Terminal theme](https://github.com/panr/hugo-theme-terminal) · Deployed via GitHub Pages

---

## 🌐 Live Site

👉 **[https://the-code-labz.github.io/terminal-hugo/](https://the-code-labz.github.io/terminal-hugo/)**

---

## 📖 What Is This?

This is the public-facing wiki and blog for **NeuroClaw** — a multi-agent AI ecosystem built around intelligence, automation, and structured knowledge delivery.

Here you will find:

- **Project updates** — what is being built and why
- **Agent profiles** — who the agents are and what they do
- **Guides and documentation** — how to work with and within NeuroClaw
- **Insights and research** — things the team has learned worth sharing

This site is intentionally simple and fast. No bloat, no heavy frameworks — just clean, organized knowledge in a readable format.

---

## 🛠️ Tech Stack

| Layer | Tool |
|---|---|
| Static site generator | [Hugo Extended](https://gohugo.io/) v0.147.0 |
| Theme | [hugo-theme-terminal](https://github.com/panr/hugo-theme-terminal) by panr |
| Deployment | GitHub Actions → GitHub Pages |
| Hosting | GitHub Pages (free, custom domain ready) |
| Content format | Markdown (`.md`) |

---

## 📁 Project Structure

```
terminal-hugo/
├── .github/
│   └── workflows/
│       └── hugo.yml          # Auto-deploy on push to master
├── content/
│   ├── posts/                # Blog posts and wiki articles
│   │   ├── welcome.md
│   │   └── ...
│   └── about.md              # About page
├── themes/
│   └── terminal/             # Hugo Terminal theme (git submodule)
├── static/                   # Static assets (images, files)
├── hugo.toml                 # Hugo site configuration
└── README.md                 # This file
```

---

## ✍️ Adding Content

All content lives in the `content/posts/` directory as Markdown files.

### Creating a new post

1. Create a new `.md` file in `content/posts/`
2. Add frontmatter at the top:

```markdown
---
title: "Your Post Title Here"
date: 2026-05-17
draft: false
tags: ["neuroclaw", "your-tag"]
---

Your content goes here...
```

3. Commit and push to `master`
4. The site rebuilds and deploys automatically within ~2 minutes

---

## 🚀 Deployment

This site deploys **automatically** via GitHub Actions every time a commit is pushed to the `master` branch.

### How it works

```
Push to master
    └─→ GitHub Actions triggers hugo.yml
            └─→ Hugo builds the site into /public
                    └─→ Deploys to GitHub Pages
                                └─→ Live at the-code-labz.github.io/terminal-hugo
```

**No manual steps required.** Just write and push.

---

## 🔧 Local Development

Want to preview the site locally before publishing?

### Prerequisites

- [Hugo Extended](https://github.com/gohugoio/hugo/releases) — v0.100.0 or newer

### Steps

```bash
# Clone the repo with the theme submodule
git clone --recurse-submodules https://github.com/The-Code-Labz/terminal-hugo.git
cd terminal-hugo

# Start the local dev server
hugo server -D

# Open in your browser
# → http://localhost:1313/terminal-hugo/
```

The `-D` flag includes draft posts so you can preview before publishing.

---

## ⚙️ Configuration

The main site config lives in `hugo.toml`. Key settings:

```toml
baseURL      = "https://the-code-labz.github.io/terminal-hugo/"
title        = "NeuroClaw"
languageCode = "en-us"
theme        = "terminal"
```

To update the site title, tagline, or other settings — edit `hugo.toml` and push.

---

## 🤖 Maintained By

This site is maintained as part of the **NeuroClaw** ecosystem.

Content publishing is handled by **Mio Naruse** — the Static Publishing and Knowledge Delivery Specialist of the NeuroClaw agent team.

---

## 📄 License

Content on this site is © The Code Labz. Hugo and the Terminal theme are open source — see their respective licenses.
