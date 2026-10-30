# pfinn.org

My homepage and learning log, built with [Astro](https://astro.build) and hosted on Vercel.
Every commit to `main` on GitHub rebuilds and publishes the site automatically.

## Add a log entry

1. Go to `src/content/log/` on GitHub and click **Add file → Create new file**.
2. Name it with the date and a few words, like `2026-11-05-dnd-site.md`. The name becomes the page address.
3. Start the file with this block (the lines between `---` are required):

```
---
title: What I did
date: 2026-11-05
summary: One sentence that shows on the homepage.
---

Write the entry here. Blank lines start new paragraphs.
Use **bold**, `code`, and - for bullet points.
```

4. Commit. The homepage puts the newest entry first.

## Add or change a project

Edit `src/data/projects.json`. Each project has a `name`, `status` (shown in the margin),
`description`, and `url` (leave it as `""` if there's no link yet). Keep the commas between projects.

## What the files do

- `src/pages/index.astro`: the homepage
- `src/pages/log/[id].astro`: the page for each log entry
- `src/layouts/Base.astro`: the shared frame (fonts, colors, analytics)
- `src/content.config.ts`: what a log entry must include
- `public/`: files served as-is, like the favicon
- `package.json`: tells Vercel this is an Astro project and which version to use

If a commit breaks the build, Vercel keeps the last working version live.
Open the failed deployment's log in Vercel and bring the error to Claude.
