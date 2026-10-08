# druedaramirez.github.io

Personal portfolio site for Daniel Rueda-Ramirez, served by GitHub Pages at
<https://druedaramirez.github.io/>.

The site is a single static page. There is no build step, no package manager and no
test suite: what is in `main` is what visitors see.

## Repository layout

| Path | What it is |
| --- | --- |
| `index.html` | The whole site: markup, CSS (one `<style>` block) and JavaScript (one `<script>` block). |
| `assets/` | Headshot, resume PDF, project downloads (PDF, `.pbix`) and project images. About 114 MB. |
| `sitemap.xml`, `robots.txt` | SEO files. Both point at the canonical URL. |
| `content/site-content.md` | Every piece of text on the site, with a template for each card type. Edit wording here. |
| `_config.yml` | Tells GitHub Pages not to publish the working documents (`README.md`, `CLAUDE.md`, `docs/`, `content/`). |
| `CLAUDE.md` | Instructions and guardrails for AI agents working in this repo. |
| `docs/WORKFLOW.md` | How work is planned, branched, reviewed and released. |
| `.github/PULL_REQUEST_TEMPLATE.md` | Template GitHub applies to every new pull request. |
| `.claude/` | Claude Code settings for this project. |

## Page structure

`index.html` has seven sections, each a `<section>` with an `id` that the navigation
links to:

`home` · `about` · `experience` · `education` · `projects` · `skills` · `contact`

External services the page depends on:

- **Google Analytics 4** (`G-N5RJ4WYL26`) for page views, downloads, contact form
  submissions and section views.
- **Formspree** for contact form delivery.
- **CDN-hosted fonts and icons**: Google Fonts, Bootstrap Icons, Tabler Icons.

## Previewing locally

Opening `index.html` in a browser works. To match how GitHub Pages serves it, run a
static server from the repo root:

```bash
python -m http.server 8000
```

Then open <http://localhost:8000/>. Check both a desktop width and a phone width
before opening a pull request, because most layout regressions on this site have
been mobile ones.

## Making a change

1. Branch from `dev` (never commit to `main` directly).
2. Make the change and preview it locally.
3. Open a pull request using the template.
4. Squash-merge into `dev`; release by merging `dev` into `main`.

The full process, including how AI agents fit into it, is in
[docs/WORKFLOW.md](docs/WORKFLOW.md). Not all of it is set up yet; that document
lists what is in place and what is still to do.

## Deployment

GitHub Pages publishes the root of `main` on every push. There is no staging
environment, so local preview is the only check before a change is live.
