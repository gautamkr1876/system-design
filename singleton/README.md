# Singleton Pattern — Q&A Reference

A clean, searchable, indexed Q&A page for revising the Singleton design pattern.

Live site (once GitHub Pages is enabled — see below):
**https://gautamkr1876.github.io/system-design/singleton/**

---

## How to Use

1. Open the live site
2. Browse the index at the top of the page
3. Click any question → jumps directly to its answer
4. Use the search bar to filter by keyword
5. Use "Back to top" to return to the index

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | The Q&A page (named `index.html` so GitHub Pages serves it automatically) |
| `README.md` | This file |
| `GITHUB-DEPLOY-GUIDE.md` | Step-by-step instructions to enable GitHub Pages |

---

## Enable GitHub Pages (one-time)

The code is already pushed. To make the live URL above work:

1. Open https://github.com/gautamkr1876/system-design/settings/pages
2. Under **Build and deployment** → **Source**: `Deploy from a branch`
3. **Branch**: `main` → folder `/ (root)` → **Save**
4. Wait ~1 minute, then visit
   **https://gautamkr1876.github.io/system-design/singleton/**

See `GITHUB-DEPLOY-GUIDE.md` for the full walkthrough.

---

## Use Locally

```bash
git clone https://github.com/gautamkr1876/system-design.git
cd system-design/singleton
open index.html
```

No build step, no dependencies — pure HTML/CSS/JS.
