# WH33ls Tech Notes

A blog for recording tech notes, insights, and solutions to technical challenges.

## About

This is a Jekyll-based blog hosted on GitHub Pages. It serves as a personal knowledge base for documenting technical learnings and sharing insights with the developer community.

## Features

- Clean, responsive design
- Blog post listing with categories and tags
- Individual post pages with navigation
- Archive page for browsing all posts
- About page
- RSS feed support
- SEO optimization

## Structure

```
├── _config.yml          # Site configuration
├── _layouts/            # HTML templates
│   ├── default.html     # Base layout
│   ├── post.html        # Blog post layout
│   └── page.html        # Page layout
├── _posts/              # Blog posts (Markdown)
├── assets/
│   └── css/
│       └── style.css    # Styles
├── about.md             # About page
├── archive.md           # Archive page
└── index.html           # Homepage
```

## Local Development

To run the site locally:

1. Install dependencies:
   ```bash
   bundle install
   ```

2. Serve the site:
   ```bash
   bundle exec jekyll serve
   ```

3. Visit `http://localhost:4000`

## Writing Posts

Create a new file in `_posts/` with the format `YYYY-MM-DD-title.md`:

```markdown
---
layout: post
title: "Your Post Title"
date: YYYY-MM-DD HH:MM:SS +0000
categories: [category1, category2]
tags: [tag1, tag2]
---

Your content here...
```

## Deployment

The site automatically deploys when changes are pushed to the main branch via GitHub Actions.

## Technologies

- [Jekyll](https://jekyllrb.com/) - Static site generator
- [GitHub Pages](https://pages.github.com/) - Hosting
- Custom CSS - Styling

## License

Content is available under [MIT License](LICENSE).