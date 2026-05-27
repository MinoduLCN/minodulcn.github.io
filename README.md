# Minodu Project — GitHub Pages Site

Project presentation and documentation site for the Minodu Project.  
Built with [Jekyll](https://jekyllrb.com/) + [Minima](https://github.com/jekyll/minima) theme, served by GitHub Pages.

🌐 **Live site:** <https://minodulcn.github.io>

---

## Pages

| Page | File | URL |
|------|------|-----|
| Home | `index.md` | `/` |
| Getting Started | `getting-started.md` | `/getting-started/` |
| Features | `features.md` | `/features/` |
| Documentation | `docs.md` | `/docs/` |
| About | `about.md` | `/about/` |

---

## Local Development

**Prerequisites:** Ruby ≥ 3.0, Bundler

```bash
bundle install
bundle exec jekyll serve
# → open http://localhost:4000
```

---

## Deployment

Every push to `main` triggers an automatic build by GitHub Pages.  
No manual step needed — just push and GitHub does the rest.

> **One-time setup:** Confirm GitHub Pages is enabled in  
> **Settings → Pages → Source → Deploy from branch → `main` / `(root)`**
