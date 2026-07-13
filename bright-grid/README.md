# Theme Concept: Bright Grid

Dark navy-to-black gradient, glowing cyan accent, Orbitron display type. A
simpler, brighter alternative to the live TallTechGuy theme — no terminal
motif, no illustration, just clean type and a glow.

This folder is **not live**. It's excluded from the build (see `_theme-concepts`
in the root `_config.yml`), so nothing here affects your actual site until you
promote it.

## What's in here

Same structure and page content as the live theme — `_layouts`, `_includes`,
`assets/css/style.css`, `index.md`, `about.md`, `games.md`, `course.md`,
`blog.md` — just restyled. If you write posts for the live site, the content
carries over directly since both themes share the same page structure.

## To make this the live theme

1. Back up or rename your current root `_layouts/`, `_includes/`, and
   `assets/css/style.css` if you want to keep them as their own concept.
2. Copy everything from this folder **except this README** up to the repo
   root, overwriting the matching files/folders.
3. Your existing `_posts/` at the root doesn't need to change — this theme's
   `post.html` and `home.html` layouts read from the same `site.posts` data
   the live theme does.
4. Push. GitHub rebuilds automatically.

## Known placeholders to wire up if promoted

- `/course/` email signup is markup only — connect it to a real form service.
- `/games/` buttons link to `#` — swap in real game URLs.
