---
layout: post
title: "Setting Up a Jekyll Blog on GitHub Pages"
date: 2025-12-28 00:00:00 +0000
categories: [tutorials, jekyll]
tags: [jekyll, github-pages, static-site, blogging]
---

GitHub Pages offers free hosting for static websites, and Jekyll is the perfect static site generator for creating blogs. Here's how I set up this blog.

## Prerequisites

Before getting started, you'll need:

- A GitHub account
- Basic knowledge of Git
- Text editor or IDE
- (Optional) Ruby installed locally for testing

## Step 1: Create a GitHub Repository

Create a new repository named `username.github.io` where `username` is your GitHub username. This special naming convention tells GitHub to host your site at `https://username.github.io`.

## Step 2: Set Up Jekyll Structure

Create the following basic structure:

```
username.github.io/
├── _config.yml
├── _layouts/
│   ├── default.html
│   └── post.html
├── _posts/
│   └── YYYY-MM-DD-title.md
├── assets/
│   └── css/
│       └── style.css
└── index.html
```

## Step 3: Configure _config.yml

The `_config.yml` file contains your site's configuration:

```yaml
title: My Tech Notes
description: A blog for recording tech notes
author: Your Name
url: "https://username.github.io"

markdown: kramdown
theme: minima
plugins:
  - jekyll-feed
  - jekyll-seo-tag
```

## Step 4: Create Layouts

Layouts define the HTML structure for your pages. Create a `default.html` layout with header, navigation, content area, and footer.

## Step 5: Write Your First Post

Posts go in the `_posts` directory with the naming convention `YYYY-MM-DD-title.md`:

```markdown
---
layout: post
title: "My First Post"
date: 2025-12-28
categories: [general]
---

Content goes here!
```

## Step 6: Add Styling

Create CSS files in `assets/css/` to style your blog. Use responsive design principles to ensure it looks good on all devices.

## Step 7: Test Locally (Optional)

Install Jekyll locally and run:

```bash
bundle install
bundle exec jekyll serve
```

Visit `http://localhost:4000` to preview your site.

## Step 8: Deploy

Commit and push your changes to GitHub:

```bash
git add .
git commit -m "Initial blog setup"
git push origin main
```

GitHub will automatically build and deploy your site!

## Key Takeaways

- Jekyll + GitHub Pages = free, fast blog hosting
- Use Markdown for easy content creation
- Customize layouts and styling to match your preference
- GitHub handles the build and deployment automatically

## Useful Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Jekyll Themes](https://jekyllthemes.io/)

Happy blogging!
