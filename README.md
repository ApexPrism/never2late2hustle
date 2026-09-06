# Never2Late2Hustle.com — static site

Plain HTML/CSS, no build step. Pages: `index.html`, `platforms.html`, `journal.html`, `about.html`, `contact.html`, plus `css/styles.css`.

## 1. Push to GitHub

From this folder:

```
git init
git add .
git commit -m "Initial N2L2H static site"
git branch -M main
git remote add origin https://github.com/<your-username>/never2late2hustle.git
git push -u origin main
```

(Create the empty repo on GitHub first if it doesn't exist yet — no README/license, so it stays empty for this push.)

## 2. Connect Cloudflare Pages

1. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
2. Pick the `never2late2hustle` repo, `main` branch.
3. Build settings: **no framework / none** — leave build command blank, output directory `/` (this is a plain static site, nothing to build).
4. Deploy.
5. Once it deploys to a `*.pages.dev` URL, go to the project's **Custom domains** tab and add `never2late2hustle.com` (and `www.never2late2hustle.com` if you want both). Since the domain's already in Cloudflare, DNS records get added automatically.

## Before you consider it launched

- [ ] Confirm the milestone stats on the homepage (tasks / hours / retirement total) — currently placeholders, marked with `TODO` comments in `index.html`.
- [ ] Wire the newsletter and contact forms in `contact.html` to a real backend (Formspree is the fastest no-server option; Cloudflare Pages Functions if you want it in-repo).
- [ ] Swap the placeholder journal entries for real posts, or link out if you're drafting them elsewhere.
- [ ] Add real social links if you want them in the footer (currently none are shown, on purpose — add back if wanted).
