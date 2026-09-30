# Repository Structure

```
my-twine-site/
│
├── .github/
│   └── workflows/
│       └── jekyll-manual.yml       # GitHub Actions — manual trigger
│
├── _layouts/
│   ├── default.html                # Base layout (header, footer, nav)
│   ├── page.html                   # Static pages
│   ├── post.html                   # Blog post layout
│   └── library.html                # Library index layout
│
├── _includes/
│   ├── head_custom.html            # Meta tags (author, og:, twitter:)
│   └── story_card.html             # Reusable story card component
│
├── _posts/                         # Blog posts (Markdown)
│   └── 2026-09-30-premier-tips.md  # Example post
│
├── library/                        # Twine stories
│   ├── aventure/
│   │   ├── story1.html             # Twine exported HTML
│   │   └── story1.md               # Sidecar: metadata for story1
│   ├── horreur/
│   │   ├── story2.html
│   │   └── story2.md
│   └── index.md                    # Library landing page
│
├── assets/
│   ├── css/
│   │   └── custom.css              # Overrides on top of Minima
│   └── images/
│       └── covers/                 # Story cover images
│           └── story1.jpg
│
├── _config.yml                     # Jekyll configuration
├── index.html                      # Homepage (latest stories + posts)
├── blog.md                         # Blog listing page
└── .nojekyll                       # NOT used here — Jekyll is active
```

## Key design decisions

- **Sidecar `.md`** : each story has a companion Markdown file with its
metadata (title, description, cover, tags). The `.html` file itself is
never touched by Jekyll — it is served as-is.
- `**library/index.md**` : the library landing page uses the `library`
layout to auto-list all stories grouped by subfolder.
- `**_includes/story_card.html**` : reusable card component used both on
the homepage (latest N stories) and the library index.
- `**_includes/head_custom.html**` : Minima supports this include natively
to inject custom `<meta>` tags without overriding the full layout.

```

```