# CLAUDE.md

Guidance for AI agents working in this repository. Read
[docs/WORKFLOW.md](docs/WORKFLOW.md) for the full planning and merge process; this
file covers what you need before touching anything.

## What this project is

A single-page personal portfolio, published by GitHub Pages from the root of `main`
at <https://druedaramirez.github.io/>. Everything lives in `index.html`: markup, one
`<style>` block and one `<script>` block. There is no build step, no dependencies to
install and no automated tests.

Two consequences follow from that:

- **A push to `main` is a production release.** There is no staging environment.
- **Almost every task edits the same file.** Parallel branches conflict easily, so
  keep changes small and scoped to one issue.

## Guardrails

- Never commit or push to `main` directly. Work on a branch cut from `dev` and go
  through a pull request.
- One issue, one branch, one pull request. Do not bundle unrelated edits.
- Commit often and push often; the remote is the backup. Do not use `git stash`.
  Commit to the branch instead, or cut a throwaway branch to experiment.
- Run `git status` before every commit and add files by name. Do not use
  `git add -A` or `git add .`; this repo has large binaries and local tool output
  that must not be swept in.
- Page content is Daniel's own resume and project history. Do not invent or
  embellish facts, numbers, dates, employers or skills. If the issue does not give
  you the wording or the fact, ask.
- Do not change the GA4 measurement ID, the Formspree endpoint, the canonical URL or
  the contact email unless the issue says to.
- Replacing a file in `assets/` changes what visitors download. Confirm before
  overwriting or deleting one.

## Where wording comes from

`content/site-content.md` is the source of truth for every piece of text on the
page. Daniel edits that file; the change is then applied to `index.html`. When asked
to update the site from it:

- Compare the content file with the page and apply only the differences. Do not
  reword, tidy or "fix" his text; report anything that looks like a mistake instead.
- Values listed once in the content file (email, phone, LinkedIn, resume file, the
  search description) appear in several places in `index.html`. Update every copy.
- If you change wording in `index.html` for any other reason, make the same change
  in the content file so the two stay in step.

The content file refers to a `/sync-content` command. It has not been written yet;
until it is, apply changes by hand following the rules above.

## Conventions in `index.html`

- **Theme**: colors come from CSS custom properties on `:root` (`--bg-dark`,
  `--bg-surface`, `--accent`, `--text-primary`, `--text-muted`, `--border`,
  `--border-accent`). Use them instead of hard-coded colors.
- **Sections**: each is `<section class="…" id="…">` with a matching link in the
  `<nav>`. If you add or rename a section, update the nav and the `sections` array in
  the scroll-tracking code at the bottom of the script.
- **Project cards**: `<article class="project-card">` inside `.projects-grid`, with a
  `.project-title`, then pairs of `.project-section-label` and
  `.project-section-content` (Context, Problem, Approach, findings or status), then
  `.project-tags` and optionally `.project-downloads`. Copy an existing card as the
  starting point. A text block with several paragraphs is several consecutive
  `.project-section-content` elements under one label.
- **In-development badge**: wrap the title in `.project-title-row` and add
  `<span class="tag tag-in-development">In Development</span>`.
- **Downloads**: links to `assets/` carry a `download` attribute and an inline
  `gtag('event', 'download', …)` call with an `event_category` and `event_label`.
  New download links need both.
- **Asset paths**: relative (`assets/…`). The resume filename contains a space and is
  URL-encoded in the markup (`Daniel%20Rueda-Ramirez_Resume.pdf`).
- **Accessibility**: the page has had an ARIA and semantic-HTML pass. Keep `alt`
  text, `aria-label`s and heading order intact when editing.
- **Indentation**: four spaces.

## Verifying a change

There is no test suite, so verification is manual. Before opening a pull request:

1. Serve the site (`python -m http.server 8000`) and load it.
2. Look at the changed area at desktop width and at phone width (about 390 px).
3. Confirm every `assets/…` path you touched resolves, and that the browser console
   is clean.
4. If you changed the contact form, do not submit real test messages to Formspree
   without asking.

Say in the pull request which of these you did. If you could not render the page,
say so plainly instead of implying it was checked.

## Commits and pull requests

- Commit subjects are imperative, sentence case, no prefix, describing the visible
  change: `Add Sectional project card, Dhiyasoft updates, and skills additions`.
- Pull requests use `.github/PULL_REQUEST_TEMPLATE.md`. Fill in the why, not only the
  what; the pull request is the written history of the change.
- Feature branches are squash-merged into `dev`. `dev` goes to `main` with a merge
  commit. Delete the branch after it merges.

## Releasing

When `dev` is merged to `main`, update `<lastmod>` in `sitemap.xml` to the release
date as part of that release.
