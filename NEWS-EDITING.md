# Updating news

Edit `_data/news.yml` and add an entry like this:

```yaml
- date: "2026-07-15"
  text: >-
    Our paper was accepted at [Conference name](https://example.com).
```

Keep dates quoted and use YYYY-MM-DD. Text can contain Markdown links.
You can add entries anywhere in the file: the site sorts them newest first.
An empty date (`date: ""`) keeps an entry unpublished.

The homepage displays the latest 10 dated entries. Once there are more than
10, a **Past news** button appears below them. It links to `/news/`, which
lists every dated entry, including the newest, in reverse chronological order.

Commit and push the data file to publish your update. You do not need a new
file in `_posts` or changes to the homepage. Existing `_posts` files are kept
to preserve their old pages, but no longer supply homepage or archive news.
