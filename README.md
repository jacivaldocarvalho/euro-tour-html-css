# EuroTour

[![Deploy website](https://github.com/jacivaldocarvalho/euro-tour-html-css/actions/workflows/deploy-pages.yml/badge.svg?branch=main)](https://github.com/jacivaldocarvalho/euro-tour-html-css/actions/workflows/deploy-pages.yml)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6)](https://developer.mozilla.org/en-US/docs/Web/CSS)

EuroTour is an educational static website built with HTML and CSS. It introduces six European destinations and links to external services for flights, accommodation, and attractions.

The project demonstrates page structure, navigation, destination cards, and responsive styling without JavaScript or frameworks. The website content is in English.

**[View the live website](https://jacivaldocarvalho.github.io/euro-tour-html-css/)**

## Requirements

- A modern web browser.
- Git to clone the repository, or a downloaded copy of the source files.
- An internet connection to load third-party images and visit external links.

No package installation, build step, or application server is required.

## View locally

```bash
git clone https://github.com/jacivaldocarvalho/euro-tour-html-css.git
cd euro-tour-html-css
```

Open `index.html` directly in your browser. To edit the page, use a text editor and refresh the browser after saving changes.

## Project structure

```text
euro-tour-html-css/
├── .github/
│   └── workflows/
│       └── deploy-pages.yml  # GitHub Pages deployment
├── css/
│   └── styles.css   # Page styles and responsive rules
├── index.html      # Website content and navigation
├── LICENSE         # MIT license
└── README.md
```

`index.html` loads `css/styles.css` using a relative path. Keep that directory structure when copying or serving the website.

## Development and validation

Edit `index.html` for content and markup, and `css/styles.css` for presentation.

There are currently no automated tests or lint checks. The GitHub Actions workflow handles deployment only; it does not validate HTML or CSS. After making changes:

1. Open the page in a browser and check that the stylesheet and images load.
2. Check the header, destination cards, and footer at narrow and wide viewport sizes.
3. Navigate through the links with the keyboard and check that focus is visible.
4. Verify that external links still point to the intended destinations.

The destination grid uses three columns above 768px, two columns from 481px to 768px, and one column at 480px or below. Check the layout at 320px, 768px, and 1280px, including with browser zoom enabled. The first keyboard link skips navigation and moves focus to the main content.

These manual checks do not replace HTML/CSS validation or a full accessibility review.

## Deployment

The deployment workflow publishes `index.html` and `css/` from `main` to GitHub Pages. It runs on pushes to `main` and can also be triggered manually from that branch. Changes on `develop` and pull requests are not published.

GitHub Pages is enabled with **GitHub Actions** as the publishing source in **Settings > Pages**. The workflow uses the `github-pages` environment and the repository's `GITHUB_TOKEN`; no additional deployment secret is required.

The website is published at https://jacivaldocarvalho.github.io/euro-tour-html-css/ with HTTPS enforced. The deployment workflow also reports the site URL.

For a fork, enable Pages with GitHub Actions as the source and update the repository-specific links and badges in this README. If deployment fails because Pages is not enabled, configure the publishing source and rerun the workflow from `main`.

## Image sources

The replacement destination photos are loaded directly from Wikimedia Commons:

- Paris: [Eiffel Tower by Mustang Joe](https://commons.wikimedia.org/wiki/File:Eiffel_Tower_(9257105067).jpg), CC0 1.0.
- Barcelona: [Barcelona panorama by Zarateman](https://commons.wikimedia.org/wiki/File:Barcelona_-_panor%C3%A1mica.jpg), CC0 1.0.

See the [CC0 dedication](https://creativecommons.org/publicdomain/zero/1.0/). The page crops these photos for display using CSS. Other destination photos and travel-service icons retain their existing external sources; their redistribution licenses have not been verified. Social links use text labels and do not depend on remote icons.

## Limitations

- The page provides informational content and external links; it does not process bookings or user data.
- All destination images and travel-service icons are loaded from third-party websites. They may become unavailable or change independently of this repository.
- Viewing the page offline does not guarantee that external images will be displayed.
- The repository's MIT license does not establish permission to redistribute third-party images. Verify their source licenses before downloading or bundling them.

## License

The repository is licensed under the [MIT License](LICENSE).

## Author

**Jacivaldo Carvalho**

Telecommunications Engineer | DevOps Engineer | SRE | Networking

[GitHub](https://github.com/jacivaldocarvalho) | [LinkedIn](https://www.linkedin.com/in/jacivaldocarvalho) | [Website](https://www.jacivaldocarvalho.com/)
