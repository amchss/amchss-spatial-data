# AMCHSS Spatial Data Resources

[![Deploy Quarto Website](https://github.com/yourusername/amchss-spatial-data/actions/workflows/deploy.yml/badge.svg)](https://github.com/yourusername/amchss-spatial-data/actions/workflows/deploy.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A professional, single-page Quarto website for distributing high-quality spatial datasets with multiple download formats, comprehensive documentation, and automated GitHub Pages deployment.

🌐 **Live Website:** [https://yourusername.github.io/amchss-spatial-data](https://yourusername.github.io/amchss-spatial-data)

## Features

- **Multiple Format Support**: Shapefile, GeoPackage, R Data, and KML formats
- **Professional Design**: Modern, responsive layout optimized for spatial data distribution
- **Complete Documentation**: Data dictionaries, usage examples, and technical specifications
- **Automated Deployment**: GitHub Actions workflow for seamless updates
- **Accessibility Compliant**: WCAG 2.1 guidelines for universal access
- **Mobile Responsive**: Optimized for all device sizes

## Quick Start

### 1. Repository Setup
```bash
# Clone the repository
git clone https://github.com/yourusername/amchss-spatial-data.git
cd amchss-spatial-data

# Install dependencies (if using Node.js features)
npm install
```

### 2. Add Your Data
- Place spatial data files in the `data/` directory
- Update download links in `index.qmd` (lines with `href="#"`)
- Modify data dictionary table to match your dataset fields

### 3. Customize Content
- Update organization name throughout files
- Modify contact information in `index.qmd`
- Adjust color scheme in `styles/custom.scss` if desired
- Update repository URLs in `_quarto.yml`

### 4. Deploy
- Push to GitHub
- Enable GitHub Pages in repository settings
- Set source to "GitHub Actions"
- Site will be available at `https://yourusername.github.io/repository-name`

## File Structure

```
amchss-spatial-data/
├── _quarto.yml                 # Main Quarto configuration
├── index.qmd                   # Single-page website content
├── styles/
│   └── custom.scss            # Professional SCSS styling
├── .github/workflows/
│   └── deploy.yml             # GitHub Actions deployment
├── data/                      # Directory for spatial data files
│   ├── formats/               # Organized by format type
│   └── documentation/         # Additional documentation
├── README.md                  # This file
├── LICENSE                    # MIT license
├── .gitignore                 # Git ignore rules
├── .nojekyll                  # GitHub Pages configuration
└── package.json               # NPM configuration (optional)
```

## Customization Guide

### For Different Organizations
1. **Find and replace** "AMCHSS" with your organization name
2. **Update colors** in `styles/custom.scss` (search for CSS custom properties)
3. **Modify contact info** in `index.qmd` footer section
4. **Update repository URLs** in `_quarto.yml` and throughout files

### For Different Data Types
1. **Update data dictionary** table in `index.qmd`
2. **Modify format descriptions** in download section
3. **Adjust usage examples** for your specific data
4. **Update technical specifications** section

### Adding New Download Formats
```markdown
::: {.download-card}
### <i class="fas fa-file-code"></i> New Format (.ext)
**Description of format**

- **File Size:** ~X.X MB
- **Best For:** Use case description
- **Includes:** What's included

[<i class="fas fa-download"></i> Download Format](#){.btn .btn-primary}
:::
```

## Development

### Local Preview
```bash
# Install Quarto
# Visit: https://quarto.org/docs/get-started/

# Preview locally
quarto preview

# Build static site
quarto render
```

### Testing
- Test responsive design on multiple screen sizes
- Validate all download links work
- Check accessibility with screen readers
- Verify code examples are syntactically correct

## Deployment

### GitHub Pages (Automatic)
1. Push to `main` branch
2. GitHub Actions automatically builds and deploys
3. Available at `https://username.github.io/repository-name`

### Manual Deployment
```bash
# Build the site
quarto render

# Deploy contents of docs/ directory to your web server
```

### Custom Domain
1. Add `CNAME` file to `docs/` directory
2. Configure DNS settings with your domain provider
3. Enable custom domain in GitHub Pages settings

## Content Management

### Updating Data
1. Replace files in `data/` directory
2. Update file sizes and dates in `index.qmd`
3. Modify "Last Updated" date in metadata
4. Push changes to trigger automatic deployment

### Version Control
- Use git tags for data releases: `git tag v1.0.0`
- Update version number in `index.qmd`
- Maintain changelog in releases

## Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details on:

- Reporting bugs or data issues
- Requesting new features
- Submitting improvements
- Code style guidelines

### Development Setup
```bash
# Fork the repository
# Clone your fork
git clone https://github.com/your-username/amchss-spatial-data.git

# Create feature branch
git checkout -b feature/your-feature-name

# Make changes and test
quarto preview

# Commit and push
git commit -m "Add feature description"
git push origin feature/your-feature-name

# Create pull request
```

## Technical Requirements

### System Requirements
- **Quarto**: Version 1.3+ required
- **R**: Version 4.0+ (for R data format support)
- **Node.js**: Version 16+ (optional, for additional tooling)
- **Git**: For version control and deployment

### Browser Support
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

### Accessibility
- WCAG 2.1 AA compliance
- Screen reader compatible
- Keyboard navigation support
- High contrast mode support

## Performance

- **Page Load Time**: <3 seconds on 3G connection
- **Lighthouse Score**: 90+ for Performance, Accessibility, SEO
- **Mobile Optimization**: Responsive design with mobile-first approach
- **SEO Optimized**: Semantic HTML, meta tags, structured data

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

- **Documentation Issues**: [Create an issue](https://github.com/yourusername/amchss-spatial-data/issues)
- **Data Questions**: Contact [spatial-data@amchss.org](mailto:spatial-data@amchss.org)
- **Technical Support**: Check existing [GitHub Issues](https://github.com/yourusername/amchss-spatial-data/issues)

## Acknowledgments

- Built with [Quarto](https://quarto.org/) by Posit
- Styled with custom SCSS and Bootstrap components
- Icons by [Font Awesome](https://fontawesome.com/)
- Fonts by [Google Fonts](https://fonts.google.com/)

---

**Last Updated:** January 2025 | **Version:** 1.0.0
