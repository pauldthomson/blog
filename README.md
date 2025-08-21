# Paul Thomson's Blog

A fast, lightweight Hugo-powered blog using the Bear Cub theme, hosted on GitHub Pages.

## About

This blog is built with [Hugo](https://gohugo.io/) and uses the beautiful [Bear Cub](https://github.com/clente/hugo-bearcub) theme, which focuses on:

- **Speed**: Minimal CSS (~5kb), no JavaScript
- **Accessibility**: High contrast ratios, keyboard navigation
- **Simplicity**: Clean, readable design inspired by Bear Blog
- **SEO**: Built-in structured data and meta tags
- **RSS**: Automatic full-content RSS feed generation

## Setup

### Prerequisites
- [Hugo Extended](https://gohugo.io/installation/) (v0.148.2 or later)
- Git

### Local Development

1. Clone the repository with submodules:
   ```bash
   git clone --recurse-submodules https://github.com/pauldthomson/blog.git
   cd blog
   ```

2. If you already cloned without submodules, initialize them:
   ```bash
   git submodule init
   git submodule update
   ```

3. Start the development server:
   ```bash
   hugo server --buildDrafts --buildFuture
   ```

4. Open your browser to `http://localhost:1313/blog/`

### Creating Content

Create a new post:
```bash
hugo new content posts/my-new-post.md
```

Create a new page:
```bash
hugo new content about.md
```

## Deployment

The site is automatically deployed to GitHub Pages using GitHub Actions when changes are pushed to the `main` or `master` branch.

The workflow:
1. Builds the site with Hugo
2. Uploads the generated static files
3. Deploys to GitHub Pages

## Theme

This blog uses the [Bear Cub](https://github.com/clente/hugo-bearcub) theme for Hugo, a lightweight theme based on Bear Blog.

### Theme Features
- Multilingual support
- Dark/light mode support
- Reply-by-email functionality
- Social card generation
- Syntax highlighting without inline styles
- Full-text RSS feeds

## Configuration

The main configuration is in `hugo.toml`. Key settings:
- `baseURL`: GitHub Pages URL
- `theme`: "hugo-bearcub"
- `params.author`: Author information for RSS and email
- `markup.highlight`: Syntax highlighting configuration

## License

Content is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).