# MoodSpoon

Essays. Feelings. Thoughts.

## Local development

```bash
npm install
npm run dev
# → http://localhost:8080
```

## Writing a new essay

1. Create a new `.md` file in `src/essays/`
2. Add frontmatter at the top:

```markdown
---
title: Your Essay Title
description: One sentence teaser shown on the list page.
date: 2026-05-13
layout: essay.njk
---

Your essay text here...
```

3. Save. Eleventy picks it up automatically and adds it to the list.

That's it. No database, no CMS, no login.

## Deploying to Vercel

1. Push this folder to a GitHub repo
2. Go to vercel.com → New Project → import your repo
3. Build command: `npm run build`
4. Output directory: `_site`
5. Add your domain `moodspoon.com` in Vercel → Domains

Every time you push new essays to GitHub, Vercel rebuilds and deploys automatically.

## Folder structure

```
src/
  essays/          ← put your .md essay files here
  css/main.css     ← all the styles
  js/main.js       ← minimal JS
  _includes/
    layouts/
      base.njk     ← site wrapper (header, footer, nav)
      essay.njk    ← single essay page template
  index.njk        ← homepage (essay list)
  about.njk        ← about page
.eleventy.js       ← Eleventy config
vercel.json        ← Vercel deployment config
```
