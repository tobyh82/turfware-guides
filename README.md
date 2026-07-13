# Turfware Help — guides site

The Turfware Help Centre, as a **docs-as-code** site. Every guide is a Markdown file in `docs/`.
Built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and deployed to **Cloudflare Pages** at `help.turfware.com`.

---

## Edit a guide (the whole workflow)

1. Edit the relevant `docs/**/*.md` file (plain Markdown).
2. Preview locally: `mkdocs serve` → open http://127.0.0.1:8000
3. Commit & push. Cloudflare Pages rebuilds and publishes automatically (~30s).

That's it — no CMS, no admin editor. Text in, site out.

## Local setup (one-time)

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve      # live preview
mkdocs build      # outputs static site to ./site
```

## Deploy — Cloudflare Pages (one-time)

1. Push this repo to GitHub (or GitLab).
2. Cloudflare dashboard → **Workers & Pages → Create → Pages → Connect to Git** → pick this repo.
3. Build settings:
   - **Build command:** `mkdocs build`
   - **Build output directory:** `site`
   - **Environment variable:** `PYTHON_VERSION = 3.11` (also pinned in `.tool-versions`)
4. Deploy. You get a `*.pages.dev` URL immediately.
5. **Custom domain:** Pages → Custom domains → add `help.turfware.com`.
   - If `turfware.com`'s DNS is on Cloudflare, the record is added for you.
   - Otherwise add a **CNAME**: `help` → `<project>.pages.dev` at your DNS provider. SSL is automatic.

Every `git push` after that = an automatic rebuild + publish.

## Media

- **Screenshots / figures:** image files in `docs/assets/`, referenced in Markdown as `![caption](../assets/name.png)`. (Relative depth: count the folders from the guide up to `docs/`.)
- **Videos:** embed the share link (Loom / Jam / YouTube) as an iframe in the Markdown — the video stays on that platform.
- `[Screenshot: …]` in a guide = a placeholder awaiting an image.

## Re-running the migration (optional)

`build_site.py` regenerated this `docs/` tree from the HelpJuice export. It needs `markdownify` and `beautifulsoup4` (`pip install markdownify beautifulsoup4`). Note: it overwrites `docs/`, so run it only for a clean re-migration.

## Structure

```
docs/            the guides (Markdown) + docs/assets (images, css, logo)
mkdocs.yml       site config, theme, nav
requirements.txt build deps (Cloudflare uses this)
```
