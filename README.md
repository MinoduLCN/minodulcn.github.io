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

### Step 1 — Install a modern Ruby

macOS ships with Ruby 2.6, which is too old for the `github-pages` gem. Use `rbenv` to manage a newer version:

```bash
brew install rbenv ruby-build

# Add rbenv to your shell (run once)
echo 'eval "$(rbenv init - zsh)"' >> ~/.zshrc
source ~/.zshrc

# Install Ruby 3.3 and pin it to this project
rbenv install 3.3.6
rbenv local 3.3.6      # creates a .ruby-version file in the repo
ruby --version          # should show 3.3.6
```

### Step 2 — Install dependencies

```bash
gem install bundler
bundle install
```

> `bundle install` reads the `Gemfile` and installs Jekyll + the same gem set GitHub Pages uses,
> so what you see locally matches what GitHub builds.

### Step 3 — Serve locally

```bash
bundle exec jekyll serve
```

Then open **http://localhost:4000** in your browser. The server watches for file changes and
rebuilds automatically — just save a file and refresh.

### Useful flags

| Flag | Effect |
|------|--------|
| `--livereload` | Auto-reloads the browser on save |
| `--drafts` | Also renders posts in `_drafts/` |
| `bundle exec jekyll build` | One-shot build into `_site/` without serving |

---

## Deployment

Every push to `main` triggers an automatic build by GitHub Pages.  
No manual step needed — just push and GitHub does the rest.

> **One-time setup:** Confirm GitHub Pages is enabled in  
> **Settings → Pages → Source → Deploy from branch → `main` / `(root)`**
