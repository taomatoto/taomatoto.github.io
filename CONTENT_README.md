# Updating Projects and Films

This site is a Jekyll/al-folio website. Most visual content is edited with Markdown files and assets inside `assets/`.

Run the local preview from the repo root:

```bash
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

Then open:

```text
http://127.0.0.1:4000/
```

## Projects / Works

The visual works page is:

```text
_pages/works.md
```

It automatically reads project files from:

```text
_projects/
```

Each project should be one Markdown file, for example:

```text
_projects/10_my_project.md
```

Use this front matter at the top:

```yaml
---
layout: page
title: AiLoupe
description: AI-assisted textile material sourcing and selection tool.
img: assets/img/my-project-cover.jpg
importance: 1
category: research
year: 2025
tools: AI / textile / design tool
related_publications: false
---
```

Field notes:

- `title`: project name shown on `/works/` and the project detail page.
- `description`: short text shown on the `/works/` card.
- `img`: cover image for the visual card. Put the file in `assets/img/`.
- `importance`: sort order. Lower number appears earlier.
- `category`: small label shown above the title.
- `year`: shown beside the category.
- `tools`: small footer line on the project card.
- `related_publications`: set to `true` only if you want related publications listed on that project page.

After the front matter, write the project detail page in Markdown/HTML:

```markdown
## Overview

Short project description.

## Process

What you designed, built, tested, or learned.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/my-project-detail-1.jpg" title="Project image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

To add images:

1. Put images in `assets/img/`.
2. Reference them without a leading slash, like `assets/img/name.jpg`.
3. Prefer `.jpg`, `.png`, or `.webp`.
4. Use simple lowercase filenames, for example `ailoupe-interface.jpg`.

To hide a project from the main navigation, do nothing extra. Projects are shown through `/works/`, not as top navigation tabs.

## Films

The films page is:

```text
_pages/films.md
```

Right now, film/gallery items are edited directly inside that file. Each item uses an `<article class="film-tile">`.

Image tile example:

```html
<article class="film-tile">
  <div class="film-tile__media">
    {% include figure.liquid loading="lazy" path="assets/img/film-still-01.jpg" alt="Film still" class="film-tile__image" %}
  </div>
  <div class="film-tile__body">
    <span>01 / still</span>
    <h2>street frame</h2>
    <p>A short note about this film still or sketch.</p>
  </div>
</article>
```

Video tile example:

```html
<article class="film-tile film-tile--wide">
  <div class="film-tile__media">
    <video autoplay muted loop playsinline preload="metadata">
      <source src="{{ '/assets/video/my-film.mp4' | relative_url }}" type="video/mp4">
    </video>
  </div>
  <div class="film-tile__body">
    <span>00 / moving note</span>
    <h2>motion study</h2>
    <p>A short note about this video fragment.</p>
  </div>
</article>
```

Tile size options:

- `film-tile`: normal tile.
- `film-tile film-tile--wide`: larger horizontal tile.
- `film-tile film-tile--tall`: taller vertical tile.

To add film images:

1. Put images in `assets/img/`.
2. Edit `_pages/films.md`.
3. Duplicate an existing image tile.
4. Change the image path, number, title, and note.

To add film videos:

1. Put `.mp4` files in `assets/video/`.
2. Edit `_pages/films.md`.
3. Duplicate the video tile.
4. Change the `<source src="...">` path.

Keep videos short and compressed for GitHub Pages. Large video files will make the site slow.

## Quick Checks

After edits, check these pages locally:

```text
http://127.0.0.1:4000/works/
http://127.0.0.1:4000/films/
```

If a new image does not appear, check:

- The file is inside `assets/img/` or `assets/video/`.
- The path spelling matches exactly.
- The filename does not contain spaces.
- The local Jekyll server has rebuilt after saving.
