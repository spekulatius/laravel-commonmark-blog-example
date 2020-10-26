---
title: "Example List"
description: "This is the example of an article list"
keywords:
  - example
  - "article list"
canonical: "https://example.com/blog/"
image: "https://example.com/some-image.png"

published: "2020-10-24 12:34:56"
modified: "2020-10-24 12:34:56"
---

# List

This is showing an example of how generate a article listing page. Any file named `index.md` will be converted to a list page automatically.

The blade-rendering function of gets the following parameters passed:

 - the complete frontmatter (merged from the `defaults.list` in [`config/blog.php`](https://github.com/spekulatius/laravel-commonmark-blog/blob/main/config/blog.php) and this pages frontmatter,
 - the commonmark-rendered content (this text) as `content`,
 - the `current_page` for the number of the page, and
 - the `total_pages` as the number of pages.

With this information your Blade-file should be able to render a complete page.


## Pagination URLs

In this example the URLs would follow:

 - `domain.com/blog/index.html`
 - `domain.com/blog/1.html`
 - `domain.com/blog/2.html`
 - `domain.com/blog/3.html`
 - etc.

With the mentioned [work-around to remove `.html`](https://github.com/spekulatius/laravel-commonmark-blog#server-configuration) these can become:

 - `domain.com/blog`
 - `domain.com/blog/1`
 - `domain.com/blog/2`
 - `domain.com/blog/3`
 - etc.

Note: The first page (here `domain.com/blog/1`) will automatically contain a canoncial URL to the variation without page number (`domain.com/blog`).
