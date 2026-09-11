# your-site

Personal site: portfolio, blog, and subject-organized study notes archive.
Built with Astro, deployed to GitHub Pages.

## Structure

- `src/content/blog/` — blog posts (markdown, one file per post)
- `src/content/archive/[subject]/` — study notes, grouped by subject folder
- `src/content/projects/` — project entries
- `src/pages/` — routes (index, /blog, /archive, /projects)
- `src/layouts/BaseLayout.astro` — shared header, footer, page shell
- `src/styles/global.css` — design tokens (colors, type)

## Before deploying

1. In `astro.config.mjs`, replace `site` and `base` with your actual
   GitHub username / repo name. If your repo is named
   `yourusername.github.io`, remove `base` entirely.
2. Update the placeholder name, bio, and links in `src/pages/index.astro`
   and `src/layouts/BaseLayout.astro`.
3. Replace the sample content in `src/content/*` with your own.

## Local dev

```
npm install
npm run dev
```

## Adding content

- New blog post: add a `.md` file to `src/content/blog/` with frontmatter
  `title`, `date`, `description`, `tags`.
- New archive note: add a `.md` file to `src/content/archive/<subject>/`
  with frontmatter `title`, `subject`, `subjectLabel`, `description`.
  The `subject` value must match the folder name.
- New project: add a `.md` file to `src/content/projects/` with
  `title`, `description`, `stack`, `url`, `date`.

## Deploy

Push to `main`. The GitHub Actions workflow in
`.github/workflows/deploy.yml` builds and publishes automatically.
In your repo's Settings → Pages, set the source to "GitHub Actions" once.
