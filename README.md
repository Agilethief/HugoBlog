# HugoBlog

A modern, fast blog powered by [Hugo](https://gohugo.io/) static site generator and hosted on GitHub Pages.

![HugoBlog Homepage](https://github.com/user-attachments/assets/eabbdee0-39ae-4727-8fa7-bcfecbb00124)

## Features

- ⚡ **Lightning Fast**: Built with Hugo, one of the fastest static site generators
- 🎨 **Beautiful Design**: Using the BeautifulHugo theme for a clean, responsive layout
- 🚀 **Automated Deployment**: GitHub Actions automatically builds and deploys on push to main
- 📝 **Easy Content Management**: Write posts in Markdown
- 🔍 **SEO Friendly**: Optimized for search engines
- 🆓 **Free Hosting**: Hosted on GitHub Pages at no cost

## Getting Started

### Prerequisites

- [Hugo](https://gohugo.io/installation/) (v0.139.0 or later)
- Git

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/Agilethief/HugoBlog.git
cd HugoBlog
```

2. Initialize and update the theme submodule:
```bash
git submodule update --init --recursive
```

3. Start the Hugo development server:
```bash
hugo server
```

4. Open your browser and visit `http://localhost:1313`

### Creating New Posts

Create a new blog post:
```bash
hugo new content/posts/my-new-post.md
```

Edit the generated file in `content/posts/my-new-post.md` and set `draft = false` when ready to publish.

### Building for Production

Build the static site:
```bash
hugo --minify
```

The generated site will be in the `public/` directory.

## Deployment

This blog uses GitHub Actions for automatic deployment. When you push to the `main` branch:

1. GitHub Actions triggers the workflow
2. Hugo builds the site
3. The static files are deployed to GitHub Pages

### Setting Up GitHub Pages

1. Go to your repository Settings > Pages
2. Under "Source", select "GitHub Actions"
3. Your site will be available at `https://agilethief.github.io/HugoBlog/`

## Project Structure

```
HugoBlog/
├── .github/
│   └── workflows/
│       └── hugo.yml          # GitHub Actions deployment workflow
├── archetypes/               # Content templates
├── content/                  # Blog content
│   ├── about/               # About page
│   └── posts/               # Blog posts
├── static/                   # Static files (images, etc.)
├── themes/
│   └── BeautifulHugo/       # Theme (git submodule)
├── hugo.toml                 # Hugo configuration
└── .gitignore
```

## Configuration

The site is configured in `hugo.toml`. Key settings:

- `baseURL`: Set to your GitHub Pages URL
- `title`: Your blog title
- `theme`: Theme name (BeautifulHugo)
- `[params]`: Theme-specific parameters
- `[[menu.main]]`: Navigation menu items

## Theme

This blog uses the [BeautifulHugo](https://github.com/halogenica/BeautifulHugo) theme, which provides:

- Responsive design
- Syntax highlighting
- Social media integration
- Tag and category support
- Clean, minimalist aesthetic

## Contributing

Feel free to fork this repository and create your own blog! To contribute to this blog:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- [Hugo](https://gohugo.io/) - The static site generator
- [BeautifulHugo](https://github.com/halogenica/BeautifulHugo) - The theme
- [GitHub Pages](https://pages.github.com/) - Free hosting