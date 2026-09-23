# Srinivas Nomula — Personal Website

A personal academic website configured for https://sivasrinivasn.github.io, with an introduction, research news, profile links, a CV, projects, and lecture notes.

The site uses **Jekyll**, Markdown, HTML, Liquid templates, and CSS. Minima is configured as the theme, but the pages use a custom shared layout and stylesheet. There is no application backend or Node build step. A small JavaScript script remembers the visitor’s light/dark mode preference.

## What to change and where

| What you want to change | File or location |
| --- | --- |
| Biography, homepage name, designation, institution text | [index.md](index.md) |
| Email destination | `mailto:` link in [index.md](index.md) |
| Scholar, LinkedIn, ORCID, and CV destinations | `social_links` in [_config.yml](_config.yml) |
| Profile icon artwork | Inline `<svg>` elements in [index.md](index.md) |
| Profile photograph | [assets/images/Srinivas.jpeg](assets/images/Srinivas.jpeg) |
| Photo dimensions, fonts, spacing, colors | [assets/css/style.css](assets/css/style.css) |
| Add or edit news | [_data/news.yml](_data/news.yml) |
| Homepage news count | `limit:10` and `updates.size > 10` in [index.md](index.md) |
| Full news archive | [news.md](news.md) |
| News row layout and displayed date format | [_includes/news-item.html](_includes/news-item.html) |
| Lecture titles, dates, and PDF paths | `lectures:` list at the top of [lectures.md](lectures.md) |
| Lecture description and study topics | HTML sections below the metadata in [lectures.md](lectures.md) |
| Lecture PDFs | `uploads/lectures/` |
| CV PDF | [uploads/cv.pdf](uploads/cv.pdf) |
| Projects / miscellaneous content | [projects.md](projects.md) / [misc.md](misc.md) |
| Header navigation, footer, theme toggle | [_layouts/default.html](_layouts/default.html) |
| Site name, description, domain, base path | [_config.yml](_config.yml) |

## Edit your introduction and links

The homepage uses HTML inside a Markdown file. Inside its `<p>` elements, use HTML links:

```html
<p>I studied at <a href="https://iiitt.ac.in/">IIIT Tiruchirappalli</a>.</p>
```

Markdown links such as `[IIIT Tiruchirappalli](https://iiitt.ac.in/)` are not processed in the existing homepage HTML blocks. They do work in ordinary Markdown content and news text.

The homepage name, designation, and institution are written directly in `index.md`; updating their similarly named settings in `_config.yml` does not automatically update that text. The shared header and footer use `site.name` from the configuration.

Contact details are part of the homepage; there is no separate Contact page.

## Resize or replace your photograph

Replace `assets/images/Srinivas.jpeg` to keep the current image path, or change the `<img src>` in `index.md` if you use a different filename.

Find the main `.profile-picture` rule in `assets/css/style.css`:

```css
.profile-picture {
    width: 225px;
    height: 260px;
    object-fit: cover;
}
```

Change `height` to make the photo shorter or taller. `object-fit: cover` crops the image to fit without stretching it. You can add `object-position: center top;` if you want to keep the top of the photograph visible.

There is a second `.profile-picture` rule inside `@media (max-width: 768px)` for phones and smaller screens. It uses `150px` for both width and height; edit that separately.

## Update profile links and your CV

Edit `social_links` in `_config.yml`:

```yaml
social_links:
  google_scholar: "https://scholar.google.com/citations?user=YOUR_ID"
  linkedin: "https://www.linkedin.com/in/YOUR_PROFILE"
  orcid: "https://orcid.org/YOUR_ORCID_ID"
  cv: "/uploads/cv.pdf"
```

These are examples: retain your real URLs when editing. An empty value (`""`) hides its icon. The email icon is separate: change its `mailto:` address in `index.md`.

Replace `uploads/cv.pdf` to update your CV without changing the link. If you rename the PDF, also update `social_links.cv`. The CV opens in a new tab, subject to the visitor’s PDF browser settings.

Icons are inline SVGs, so separate image downloads are unnecessary. Their size is set in `.social-links svg` in the stylesheet and in the SVG width/height attributes. They currently use 18px. `currentColor` and `var(--section-bg)` let icons follow the site’s theme.

## Add news without creating a new page

Add an entry to `_data/news.yml`:

```yaml
- date: "2026-09-23"
  text: >-
    Our paper was accepted at [Conference name](https://example.com).
```

- Keep dates quoted in `YYYY-MM-DD` format and use spaces for indentation.
- Write the announcement below `text: >-`; Markdown links are supported.
- Entries are sorted newest first, regardless of where you put them in the file.
- The homepage shows the latest **10** dated entries.
- When there are **more than 10**, a **Past news** button links to `/news/`, which shows all entries, including the newest.
- `date: ""` omits an entry from both lists. This is not private storage: the text still exists in the repository/data file.
- Future dates are not scheduled automatically; any nonempty date is included.

No `_posts` folder or individual news `.md` files are needed.

To change the homepage count, update **both** `limit:10` and `updates.size > 10` in `index.md`. The archive has no limit. To show full dates instead of month/year, change `%b %Y` to `%d %b %Y` in `_includes/news-item.html`.

## Add lecture PDFs

1. Put your PDF in `uploads/lectures/`, for example `introduction.pdf`.
2. Add an entry under `lectures:` in the YAML metadata at the top of `lectures.md`:

   ```yaml
     - title: Introduction
       date: "23 Sep 2026"
       pdf: /uploads/lectures/introduction.pdf
   ```

3. Commit the PDF and the edited page together.

The title becomes a blue link opening in a new tab when the matching PDF exists. Until then, the page displays “notes coming soon.” Filenames and capitalization must match exactly. Use short filenames without spaces.

Lecture numbers follow the order of the entries, so reorder the list to change the study sequence. Use `date: ""` to omit a date. The separate **Study Topics** and **Description** sections below the list are edited manually.

## Change the header, footer, or appearance

All pages use `_layouts/default.html`. Edit the active navigation list there to add or remove header links. The homepage displays a home icon; other pages display your name. Both link back to the homepage.

To add a new page, create a Markdown file with metadata like:

```yaml
---
layout: default
title: Publications
permalink: /publications/
---
```

Write the content below it, then add a navigation link in the layout if desired. Use the page’s permalink, including the trailing slash.

Useful stylesheet selectors:

| Selector | Controls |
| --- | --- |
| `:root` / `[data-theme="dark"]` | Light/dark palette, link colors, muted text, borders |
| `.profile-about-section` | Photo and introduction layout |
| `.about-content h1` / `.bio` | Name and biography text |
| `.social-links` | Profile icon row and spacing |
| `.news-section h2` | Homepage “News & Updates” heading size |
| `.news-item` / `.news-content p` | News spacing and body text size |
| `.lecture-page` rules | Lecture headings, lists, and links |
| `nav` / `.home-icon-button` | Navigation bar and home icon |
| `footer` | Copyright text size and spacing |

The footer stays at the bottom on short pages through the flex layout on `body` and `main`. Keep those rules when adjusting its padding. Media queries near the bottom of the stylesheet override some sizes on smaller screens.

## Publish and check your changes

Save the files, review `git diff`, then commit and push the files you changed to the repository’s configured publishing branch. Include new PDFs and images, not just their links. The publishing branch and build method are managed in the repository’s GitHub Pages configuration, not in this README; this checkout has no custom deployment workflow.

After the deployment finishes, check the homepage and the changed pages, including a narrow screen and both themes. Confirm PDF links open and the shared navigation matches across pages.

If you see an older page, confirm the latest deployment succeeded and try a hard refresh: **Ctrl+Shift+R** on Windows/Linux or **Cmd+Shift+R** on macOS.

## Local preview and troubleshooting

This repository does not currently include a `Gemfile` or a pinned local build environment. If Jekyll and the required theme dependencies are already installed, run `jekyll serve` from this directory and open the local URL it prints. Restart it after editing `_config.yml`. Opening `.md` files directly in a browser will not render Liquid or Jekyll output.

- **Literal `[text](url)` in the bio:** use an HTML `<a>` link inside the existing HTML blocks.
- **PDF shows “coming soon”:** check the file exists and its exact path matches the lecture metadata.
- **Past news button missing:** it appears only when there are more than 10 dated updates.
- **Build fails after editing:** check YAML indentation/quotes and matching Liquid `{% if %}` / `{% endif %}` and `{% for %}` / `{% endfor %}` tags.
- **Inconsistent headers:** confirm all pages use `layout: default`, then check deployment and browser caching before editing individual pages.
