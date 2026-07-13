# Theme Concepts

This folder is intentionally kept out of the live build (see `_theme-concepts`
in the root `_config.yml` exclude list, plus Jekyll's own default behavior of
skipping underscore-prefixed folders).

Use it to stash other theme ideas without them ever going live:

```
_theme-concepts/
├── minimal-theme/
│   ├── _layouts/
│   ├── _includes/
│   ├── assets/
│   └── notes.md
└── another-idea/
    └── ...
```

Each subfolder can be a fully self-contained theme concept — its own layouts,
includes, and styles. None of it gets touched by the live build at the repo
root.

**To promote a concept to live:** move its contents to the repo root
(replacing `_layouts/`, `_includes/`, `assets/`, and `_config.yml` values),
or start a new branch from this repo and build it out there instead if you
want to preview it live before committing.
