# Brow Studio Anna — úprava a laminace obočí, Praha

Static concept page exported from site-factory (brows-studio / quick). Open `index.html` in a browser — no build needed.

## Publish on GitHub Pages

```bash
cd clients/brows-studio/final
git init && git add . && git commit -m "Concept page"
git branch -M main
gh repo create brows-studio --public --source=. --push          # or create the repo on github.com and: git remote add origin … && git push -u origin main
gh api -X POST repos/{owner}/brows-studio/pages -f "source[branch]=main" -f "source[path]=/"   # or: repo Settings → Pages → Deploy from a branch → main / root
```

After changes in the prototype, export again (`npm run final -- brows-studio`) and push: `git add -A && git commit -m "Update" && git push` — the export keeps this folder's `.git`.

The page appears at `https://<your-user>.github.io/brows-studio/` after a minute. Re-export with `--url=https://<your-user>.github.io/brows-studio/` so link previews show `og.jpg`.

Search engines are told not to index it (`noindex`). The edit panel is off.
