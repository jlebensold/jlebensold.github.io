# lebensoldweb

Family website built with Jekyll and the Minima theme.

## Prerequisites

- Ruby (version 2.7 or higher)
- Bundler gem (`gem install bundler`)

## Initial Setup

1. Clone the repository
2. Install dependencies:
```bash
bundle install
```

## Running the Site Locally

To preview the site locally with live reloading:

```bash
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`

To run with drafts visible:
```bash
bundle exec jekyll serve --drafts
```

**Important:** If you modify `_config.yml`, you must stop and restart the server for changes to take effect.

## Updating Content

### Editing Existing Pages

The main content pages are markdown files in the root directory:
- `jon.md` - Jonathan's page
- `julian.md` - Julian's page
- `esther.md` - Esther's page
- `suzanne.md` - Suzanne's page
- `index.markdown` - Home page

To update a page:
1. Edit the corresponding `.md` file
2. Save your changes
3. If the local server is running, it will automatically rebuild
4. Refresh your browser to see the changes

### Adding a New Page

1. Create a new markdown file (e.g., `newpage.md`) in the root directory
2. Add front matter at the top:
```yaml
---
layout: page
title: Page Title
permalink: /newpage.html
---
```
3. Add your content below the front matter
4. The page will automatically appear in the navigation

### Updating Site Configuration

Edit `_config.yml` to change:
- Site title
- Description
- Base URL
- Social media links
- Theme settings

Remember to restart the Jekyll server after modifying this file.

## Building for Production

To build the static site for deployment:

```bash
bundle exec jekyll build -d ../jlebensold.github.io
```

This generates the site in the `_site/` directory.

## Project Structure

```
.
├── _config.yml          # Site configuration
├── _site/              # Generated site (do not edit directly)
├── Gemfile             # Ruby dependencies
├── index.markdown      # Home page
├── jon.md              # Jonathan's page
├── julian.md           # Julian's page
├── esther.md           # Esther's page
├── suzanne.md          # Suzanne's page
└── 404.html            # Custom 404 page
```

## Useful Commands

- `bundle exec jekyll serve` - Run development server
- `bundle exec jekyll build` - Build the site
- `bundle exec jekyll clean` - Clean the build directory
- `bundle update` - Update dependencies

## Troubleshooting

- If you encounter dependency issues, try running `bundle update`
- Clear the cache with `bundle exec jekyll clean` if you see stale content
- Make sure you're using `bundle exec` before Jekyll commands to use the correct gem versions