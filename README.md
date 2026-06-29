# Remaking School — website

A small, static website. Three files, no build step, no framework. It loads fast,
it's yours to keep, and you can move it anywhere.

```
index.html    →  the page and all its words
styles.css    →  the look (colors, fonts, spacing) — brand tokens at the top
README.md     →  this file
```

---

## Editing the words

Open `index.html`. Each section is marked with a comment banner, e.g.
`<!-- ═══ HERO — headline + opening line ═══ -->`. Find the section you want,
change the text between the tags, save. That's it.

To swap the placeholder portrait for a real photo: drop your headshot in this
folder (say `headshot.jpg`) and follow the note next to the `PORTRAIT` block in
`index.html`.

## Changing the look

Open `styles.css`. The very top is a block labeled **BRAND TOKENS**. Every color,
typeface, and key spacing value lives there once — change a value and it updates
across the whole site. These are the exact values from your brand palette. You
rarely need to touch anything below that block.

---

## How it goes live

The site is hosted on a static host (Cloudflare Pages or Netlify) connected to a
GitHub repository. The host watches the repo: **every time a change lands in the
repo, the live site rebuilds itself within a few seconds.** No uploading, no
exporting. Edit → save → push → it's live.

## Working with Claude Code

This is the fast loop. With Claude Code installed (see setup below), open a
terminal in this folder and run:

```
claude
```

Then just say what you want in plain English — "make the hero headline larger,"
"add a testimonials section," "change the maroon a shade warmer." Claude edits the
actual files here, and (if you ask) commits and pushes so the change goes live on
its own. You stay in control: review anything before it's pushed, and edit the
files yourself anytime.

---

## One-time setup

1. **Put this folder in a GitHub repo.** Create a free account at github.com, make
   a new repository (e.g. `remaking-school`), and upload these files — or let
   Claude Code do the `git init` / first commit / push for you.

2. **Connect a host.** Sign in to Cloudflare Pages (or Netlify) with your GitHub
   account, pick this repo, and deploy. For a static site there's nothing to
   configure — no build command, output is the repo root. You'll get a temporary
   URL immediately.

3. **Point your domain.** Add `remakingschool.com` as a custom domain in the host's
   dashboard and follow its DNS instructions. You can keep the domain registered
   wherever it is and just change where it points, or move it over entirely.

After that, the loop in "How it goes live" is all you need.

> **Note:** Claude Code requires a paid Claude plan (Pro or higher). The free plan
> doesn't include it. You can also keep iterating in the regular Claude chat and
> push changes manually — same result, one extra step per round.
