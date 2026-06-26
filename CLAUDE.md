# VORSO Website (`vosro-site`) — working rules

The marketing site for VORSO, served at **https://vorso.org** via **GitHub Pages**.
Static HTML/CSS (no build step). All CSS is inline in a `<style>` block at the top
of each page. Pages: `index.html` (landing), `privacy.html`, `terms.html`, `404.html`.

## Git workflow — MANDATORY

Never commit feature work directly to `main`. For every change:

1. **Branch** off `main` with a descriptive name (`feat/…`, `fix/…`, `chore/…`).
2. **Commit** the work and push the branch.
3. **Open a PR** into `main` (`gh pr create`).
4. **Merge** the PR into `main`, then delete the branch (`gh pr merge --squash --delete-branch`).

Merging to `main` **auto-deploys to production** (vorso.org) in ~20s. Treat every
merge as a production release: after merging, verify the live site
(`curl https://vorso.org/…`) before considering the task done.

## Notes

- Custom domain via `CNAME`; `.nojekyll` present so `.well-known/` is served.
- Social accounts: Instagram & X both **@playvorso**.
- This repo is **public** — never put secrets, internal notes, or business strategy here.
- Legal claims on the site (privacy/terms) must match what the app actually does —
  verify against the app code before publishing.
