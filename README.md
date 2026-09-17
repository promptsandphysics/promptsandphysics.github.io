# Physics and Prompts

Source for <https://physicsandprompts.github.io/> — a communal blog for
high-energy theory and quantum gravity, on how AI is changing the practice.

Built with **Jekyll**, which GitHub Pages compiles automatically. You never
need to build anything locally: commit a file, push, and the site rebuilds in
about a minute.

AI Disclosure: This site is based off of proofsandprompts.com, and was built using Claude.

---

## Before launch: the checklist

Five things are deliberately left as placeholders.

- [ ] **Submission address.** `_config.yml` → `email:` is
      `physicsandprompts@example.com`. Replace with the real inbox.
- [ ] **Your bio.** `_data/editors.yml` contains a stub entry for you that says
      REPLACE THIS TEXT. It is a placeholder, not a bio anyone approved.
- [ ] **Delete the sample posts.** `_posts/2026-09-15-sample-*.md` and
      `_posts/2026-09-13-sample-*.md`. They render with an orange "sample"
      banner so they cannot be mistaken for real contributions.
- [ ] **Clear the sample newsfeed entries** in `_data/newsfeed.yml`.
- [ ] **Turn on comments** — see below.

`_posts/2026-09-17-why-this-exists.md` is a genuine opening post, not a sample.
Edit it and sign it properly, or delete it.

---

## Adding a post

Create one file in `_posts/`, named `YYYY-MM-DD-some-slug.md`. The date in the
filename is what orders the site, and **a post dated in the future will not
appear** until that date arrives.

```markdown
---
title: "What the title is"
date: 2026-09-20
author: "Jane Physicist"
author_url: "https://example.edu/~jane"   # optional, links the byline
affiliation: "Some University"            # optional
career_stage: "Postdoc"                   # optional
tags: [Reflection, Teaching]
excerpt_override: "One sentence shown on listing pages."
ai_disclosure: >-                         # optional, renders in a marked box
  Used for copy-editing only.
---

Your text here, in Markdown.
```

Only `title`, `date` and `author` really matter; everything else is optional.

Then:

```bash
git add . && git commit -m "Post: what the title is" && git push
```

Everything else updates itself — the front page, `/posts/`, `/tags/`,
`/contributors/`, the RSS feed, and the previous/next links on each post.

### Anonymous posts

Set `author: "Anonymous"` and use `career_stage` and a country in
`affiliation`. Omit `author_url`.

---

## Mathematics

LaTeX renders client-side through MathJax. Inline `$g_{\mu\nu}$`, display:

```latex
$$
S_A = \frac{\text{Area}(\gamma_A)}{4 G_N}
$$
```

Markdown is set to GitHub-flavoured mode specifically so that subscripts like
`x_1` and `y_2` in the same line do not get turned into italics. If a stubborn
expression still renders wrongly, wrap it in `\(` `\)` instead of `$` `$`.

A literal dollar sign in prose should be written `\$`.

---

## Tags

Just list them in a post's `tags:`. The `/tags/` page builds itself from
whatever has been used. Tags are case-sensitive, so `Teaching` and `teaching`
become two separate tags — keep them Capitalised.

---

## Comments (giscus)

Comments are stored as GitHub Discussions in this repo. Currently **off**.
To enable:

1. Repo **Settings** → **General** → **Features** → tick **Discussions**.
2. In the new **Discussions** tab, create a category called **Comments**
   (choose the *Announcement* format so only maintainers can open threads).
3. Install the [giscus app](https://github.com/apps/giscus) on this repo.
4. Go to <https://giscus.app>, enter `physicsandprompts/physicsandprompts.github.io`,
   pick the **Comments** category, and copy the `data-repo-id` and
   `data-category-id` it generates.
5. Paste both into `_config.yml` under `giscus:` and set `enabled: true`.

Until step 5, each post shows a short "comments are not enabled yet" note
instead. Readers need a GitHub account to comment.

---

## The newsfeed

Edit `_data/newsfeed.yml`. Entries sort by date automatically, newest first:

```yaml
- date: 2026-09-20
  title: "What happened"
  url: https://example.org/thing
  summary: >-
    Two or three sentences of context.
```

The "Elsewhere" links at the bottom of that page come from `_data/links.yml`.

---

## Editing pages

| Page | File |
|------|------|
| Front page | `index.html` |
| About | `about.md` |
| Submit | `submit.md` |
| Newsfeed | `newsfeed.md` + `_data/newsfeed.yml` + `_data/links.yml` |
| Posts index | `posts.html` (generated) |
| Tags | `tags.html` (generated) |
| Contributors | `contributors.html` (generated from post front matter) |

Design lives in one file: `assets/css/style.css`. The colour palette is the
block of CSS variables at the top, with dark-mode overrides right below it.

---

## If a push does not show up

GitHub Pages builds after every push and it can fail silently from your
terminal's point of view. Check the repo's **Actions** tab — a red X there
will name the file and line that broke the build. The usual culprits are a
missing `---` block at the top of a post, a stray tab character in a `.yml`
file, or a colon inside an unquoted `title:`.

## Optional: previewing locally

Not required, and it needs Ruby installed.

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>.
