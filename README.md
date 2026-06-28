# AIRLab Hassen — production-ready GitHub Pages site

This repository is prepared for the clean GitHub Pages user/organization URL:

```text
https://AIRLabHassen.github.io/
```

For that URL to work, the repository must be named exactly `AIRLabHassen.github.io` and it must be owned by the GitHub user or organization named `AIRLabHassen`.

## What is included

- Static HTML pages ready for GitHub Pages.
- Root-relative asset paths such as `/assets/img/...` for stable deployment at the clean root domain.
- Localized figure assets in `assets/img/`; old Google-hosted figure URLs were replaced.
- SEO files: `robots.txt`, `sitemap.xml`, canonical URLs, Open Graph metadata, and Twitter card metadata.
- `.nojekyll` to serve the static files exactly as written.
- GitHub Actions workflow at `.github/workflows/deploy-pages.yml`.
- `DEPLOYMENT.md` with step-by-step publishing instructions.
- `figure-manifest.csv` documenting every figure and the requested GitHub assets directory:
  `https://github.com/InteractiveRoboticsHassen/AIRLabHassen.github.io/tree/main/assets/img`

## Important image-path note

The live website uses `/assets/img/...` paths. This is the production-safe choice for GitHub Pages because GitHub `tree/main/...` URLs are directory-browsing pages, not direct image files.

After deployment, a figure such as:

```text
/assets/img/futuristic-robotics-ai-lab-scene.png
```

will resolve publicly as:

```text
https://AIRLabHassen.github.io/assets/img/futuristic-robotics-ai-lab-scene.png
```

## Local preview

Because the site uses root-relative paths, preview it with a local web server from the repository root:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```
