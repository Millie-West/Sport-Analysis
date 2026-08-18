# Ticket Builder — Deploy Guide

This folder contains one file: `index.html`. It's fully self-contained (no server,
no database, no build step), so "deploying" it just means putting that file
somewhere with a public URL.

## Fastest: Netlify Drop (no account needed for a quick test)
1. Go to https://app.netlify.com/drop
2. Drag this whole folder (or just `index.html`) onto the page
3. Netlify gives you a live URL immediately (e.g. `random-name-123.netlify.app`)
4. Optional: create a free Netlify account afterward to keep the site and set a custom subdomain

## Free and permanent: GitHub Pages
1. Create a new GitHub repository (public)
2. Upload `index.html` to the root of the repo
3. Go to Settings → Pages → set Source to "Deploy from a branch", branch `main`, folder `/root`
4. GitHub gives you a URL like `https://yourusername.github.io/repo-name/`
5. Any time you edit the tool, just replace `index.html` in the repo — the live site updates automatically

## Also free: Vercel
1. Go to https://vercel.com, sign in, click "Add New → Project"
2. Choose "Deploy without Git" / drag-and-drop, and drop `index.html`
3. Vercel gives you a live URL, and you can add a custom domain later if you want one

## Notes
- No environment variables, API keys, or backend are required — everything runs in the visitor's browser.
- Saved/starred tickets only persist for the current browser tab session; they are not stored on a server (by design — nothing here touches a database).
- If you later want a custom domain (e.g. `ticketbuilder.yourdomain.com`), all three hosts above support adding one for free; you just point a DNS record at them.
