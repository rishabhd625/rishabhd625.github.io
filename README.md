# Rishabh's Portfolio

A Jekyll-powered portfolio website hosted on GitHub Pages.

## About

This is a personal portfolio website built with Jekyll, featuring:
- Responsive design using the Minima theme
- Project showcase with collection support
- SEO optimization
- RSS feed generation

## Local Development

To run this site locally:

1. Install dependencies:
```bash
bundle install
```

2. Start the Jekyll server:
```bash
bundle exec jekyll serve
```

3. Open your browser to `http://localhost:4000`

## Customization

### Update Site Information

Edit `_config.yml` to customize:
- Site title and description
- Your email and social media links
- Theme and plugin settings

### Customize Homepage

Edit `index.md` to update:
- About Me section
- Skills list
- Contact information

### Add Projects

1. Create a new markdown file in the `_projects` directory
2. Add front matter with title, description, and technologies
3. Write project details in markdown
4. The project will automatically appear on the projects page

Example project front matter:
```yaml
---
title: My Project
description: A brief description
technologies:
  - React
  - Node.js
github_url: https://github.com/username/repo
---
```

## Deployment

This site is automatically deployed to GitHub Pages when changes are pushed to the main branch.

View it at: https://rishabhd625.github.io

## License

MIT License