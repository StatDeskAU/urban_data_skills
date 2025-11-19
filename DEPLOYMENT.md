# GitHub Pages Deployment Guide

This repository is configured for GitHub Pages deployment using Jekyll.

## Enabling GitHub Pages

To enable GitHub Pages for this repository:

1. Go to the repository **Settings** on GitHub
2. Navigate to **Pages** in the left sidebar
3. Under "Build and deployment":
   - **Source**: Select "Deploy from a branch"
   - **Branch**: Select `main` (or your preferred branch) and `/ (root)`
   - Click **Save**

GitHub will automatically build and deploy the site within a few minutes.

## Accessing the Site

Once enabled, the site will be available at:
- `https://statdeskau.github.io/urban_data_skills/`

## Site Structure

The site includes:

- **index.md**: Home page with overview of Urban Data Network and urban data skills
- **about.md**: Background information about the initiative and approach
- **resources.md**: Comprehensive list of Australian data sources and learning resources
- **_config.yml**: Jekyll configuration file
- **Gemfile**: Ruby dependencies for local development

## Local Development (Optional)

To run the site locally for testing:

1. Install Ruby (version 2.7 or higher)
2. Install Bundler: `gem install bundler`
3. Install dependencies: `bundle install`
4. Run Jekyll: `bundle exec jekyll serve`
5. View site at: `http://localhost:4000`

## Updating Content

To update the site content:

1. Edit the relevant `.md` files (index.md, about.md, resources.md)
2. Commit and push changes to GitHub
3. GitHub Pages will automatically rebuild and deploy the site

## Theme

The site uses the default `minima` theme, which is clean, responsive, and works well for documentation sites. To customize:

- Edit `_config.yml` to change site settings
- Add custom CSS in `assets/css/style.scss` (create this file if needed)
- Override theme layouts by creating files in `_layouts/` directory

## Adding New Pages

To add a new page:

1. Create a new `.md` file in the root directory
2. Add front matter at the top:
   ```yaml
   ---
   layout: page
   title: Your Page Title
   permalink: /your-page/
   ---
   ```
3. Add the page to navigation in `_config.yml` under `header_pages`

## Troubleshooting

If the site doesn't build:
- Check the **Actions** tab in GitHub for build errors
- Ensure all front matter is properly formatted (YAML between `---` markers)
- Verify that `_config.yml` is valid YAML syntax

## Support

For issues specific to this resource, contact the Planning Institute of Australia through their official channels.

For GitHub Pages technical issues, see: [GitHub Pages Documentation](https://docs.github.com/en/pages)
