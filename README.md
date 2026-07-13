# pagethemes-jekyll

The live theme is **Earthy Blue** — earthy slate-blue background, white lettering, warm gold accent, an animated grid that drifts and fades in the background, a "Right now" panel, a credentials strip, and a Projects section. It lives at the root of this repo and is what GitHub Pages actually builds and serves.

Older theme concepts live in `_theme-concepts/` — including the original Fjord Terminal theme this replaced, and the Bright Grid concept. See that folder's own README for how to bring one back.

## 1. Publish it (no local setup required)

1. Create a new GitHub repo — name it `yourusername.github.io` if you want the site at the bare root, or anything else if you're fine with `yourusername.github.io/repo-name`.
2. Upload every file/folder in this project to the repo, keeping the folder structure exactly as-is (`_layouts`, `_includes`, `_posts`, `assets`, etc. all matter — Jekyll looks for these exact names).
3. Open **`_config.yml`** and update the `url` (and `baseurl` if your repo isn't named `username.github.io`).
4. In the repo, go to **Settings → Pages** → set source to your default branch, root folder.
5. GitHub builds the site automatically. Give it a minute or two, then check the URL shown in Settings → Pages.

No Ruby, no local build step needed for this — GitHub runs Jekyll for you on every push.

## 2. Writing a new post

Add a new markdown file inside `_posts/`, named exactly like this:

```
YYYY-MM-DD-your-post-title.md
```

With this at the top:

```
---
title: "Your Post Title"
date: 2026-07-20
tags: [governance, security]
---

Write your post here in normal markdown. Headers, lists, links, bold —
all of it works.
```

Push it, and it shows up automatically on the homepage and `/blog/` — newest first, no other steps.

## 3. Editing pages

- `about.md`, `games.md`, `course.md` — plain markdown, edit directly.
- `index.md` — the homepage. The hero and post list are built into the `home` layout, so this file usually stays empty; anything you add here appears *below* the post list.

## 4. Previewing locally (optional)

If you want to see changes before pushing:

```
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`. Requires Ruby installed (`ruby -v` to check).

## 5. Things to wire up before this feels "done"

- The email signup on `/course/` is just markup — connect it to Gumroad, Formspree, or similar before relying on it. See our notes on low-cost course/document sales if you haven't picked one yet.
- The two game buttons on `/games/` link to `#` — swap in the real URLs once your games are hosted.
- The four "View project" links on the homepage link to `#` — point them at real write-ups or drop them for projects without one.
- `_config.yml` → `url` must be correct or CSS/fonts/links can break in production even though they work fine locally.
- The animated grid background respects `prefers-reduced-motion` automatically — no action needed, but good to know if you're testing and it looks static on a machine with that setting on.
