# Handoff — UniManitoba.store

## What this is
UniManitoba.store is the working name for a University of Manitoba campus-focused marketplace ("buy, sell, swap campus stuff"). Currently a static, front-end-only prototype — no backend, no database, no build tools.

## Files
| File | Purpose |
|------|---------|
| `index.html` | Landing / marketplace home page |
| `info.html` | Info & policies page |
| `post-a-listing.html` | "Post a listing" form page |
| `404.html` | Custom 404 page |
| `handoff.md` | This doc |

## Tech stack
- Plain HTML + embedded CSS + vanilla JS (no frameworks, no build step)
- Google Fonts (Fraunces, Courier Prime, Inter, Caveat)
- Dark/light theme via CSS variables + `prefers-color-scheme`

## How to run locally
Open `index.html` in a browser. No server or dependencies required.

## Git setup
- Repo folder: `UniversityMarketPlace/` (nested inside the parent UniMarketplace-cavking folder — note the parent is NOT a git repo)
- Remote: `https://github.com/Cavking-cmd/UniversityMarketPlace.git`
- Branch: `main`
- Commit author: JohnAyo <ayooluwaokeyode@gmail.com>
- `git push --force origin main` was used once to replace stale remote history with the current project

## Credentials & access
- GitHub auth is handled by **Git Credential Manager** on Windows (Control Panel → Credential Manager → Windows Credentials → `git:https://github.com`). Tokens/live values are intentionally NOT recorded here.
- To switch which GitHub account pushes: delete the stored credential (`cmdkey /delete:git:https://github.com`) and let the next push prompt for the other account.
- Suggested: rotate/revoke the previously exposed `gho_…` token in GitHub → Settings → Developer settings → Personal access tokens, since it was printed in a chat session.

## Known issues / notes
- A PAT token was exposed during setup — revoke and regenerate (see above).
- No README yet — add one when ready.
- No hosting/local dev server orchestration yet; deploy target (GitHub Pages / Netlify / similar) not determined.

## Next steps (suggestions)
1. Decide hosting + enable HTTPS
2. Add a README
3. Wire the post-a-listing form to real storage (Supabase/backend) when ready
4. Wire up GitHub Pages or similar so the site is live