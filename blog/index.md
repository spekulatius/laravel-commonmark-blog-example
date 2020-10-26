---
title: "Example List"
description: "This is the example of an article list"
keywords:
  - example
  - "article list"
image: "https://example.com/some-image.png"

published: "2020-10-24 12:34:56"
modified: "2020-10-24 12:34:56"
---

# List

This is showing an example of how generate a article listing page. Any file named `index.md` will be converted to a list page automatically.

The blade-rendering function of gets the following parameters passed:

 - the complete frontmatter (merged from the `defaults` in [`config/blog.php`](https://github.com/spekulatius/laravel-commonmark-blog/blob/main/config/blog.php) and this page frontmatter,
 - the CommonMark-rendered content (this text) as `$content`,
 - the `$current_page` for the number of the page,
 - the `$total_pages` as the total number of pages, and
 - the `$articles` of the current page.

With this information your Blade-file should be able to render a complete listing page with pagination.


## Pagination URLs

If for example three pages of articles are rendered the URLs would be:

 - `domain.com/blog/index.htm`
 - `domain.com/blog/1/index.htm`
 - `domain.com/blog/2/index.htm`
 - `domain.com/blog/3/index.htm`

Which would be served by most web-servers as the following:

 - `domain.com/blog`
 - `domain.com/blog/1`
 - `domain.com/blog/2`
 - `domain.com/blog/3`

**Note:** The first file (here `blog/1/index.htm`) will be a copy of the `blog/index.htm` file. Therefore it will automatically contain a canoncial URL to the variation without page number (`domain.com/blog`).
