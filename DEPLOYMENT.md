# Deployment process for AIRLab Hassen

## Goal

Publish the site at:

```text
https://AIRLabHassen.github.io/
```

The current project-style URL happens when the repository is under another owner, for example:

```text
https://interactiveroboticshassen.github.io/AIRLabHassen.github.io/
```

To remove the owner/repository path from the URL, the site must be deployed as a GitHub Pages user/organization site.

## Step 1 — Prepare the GitHub owner

Use a GitHub user or organization named exactly:

```text
AIRLabHassen
```

Domain names are case-insensitive, but the repository/owner naming should match this branding as closely as possible.

## Step 2 — Create or transfer the repository

Create a repository under that owner named exactly:

```text
AIRLabHassen.github.io
```

The repository name is what makes GitHub Pages serve the site from the root `github.io` URL instead of a project subpath.

## Step 3 — Upload the site files

Unzip the production package and upload the contents of the unzipped folder to the root of the repository.

Do not upload the zip file itself and do not place everything inside an extra nested folder. The repository root should contain files like this:

```text
index.html
research.html
publications.html
assets/
.github/
.nojekyll
robots.txt
sitemap.xml
```

## Step 4 — Commit to the `main` branch

Commit all files to the `main` branch.

## Step 5 — Enable GitHub Pages

Recommended production path:

1. Open the repository on GitHub.
2. Go to **Settings**.
3. Go to **Pages**.
4. Under **Build and deployment**, set **Source** to **GitHub Actions**.
5. The included workflow `.github/workflows/deploy-pages.yml` will deploy the static site whenever you push to `main`.

Alternative simple path:

1. Go to **Settings → Pages**.
2. Set **Source** to **Deploy from a branch**.
3. Select `main` and `/root`.
4. Save.

Use only one Pages publishing method at a time.

## Step 6 — Check deployment

Open the repository **Actions** tab and confirm that the Pages deployment completed successfully.

Then visit:

```text
https://AIRLabHassen.github.io/
```

## Step 7 — Enforce HTTPS

In **Settings → Pages**, enable **Enforce HTTPS** when the option is available.

## Step 8 — Verify assets

Check that image URLs load from:

```text
https://AIRLabHassen.github.io/assets/img/...
```

The source assets are also documented in `figure-manifest.csv` with the requested GitHub directory:

```text
https://github.com/InteractiveRoboticsHassen/AIRLabHassen.github.io/tree/main/assets/img
```

## Step 9 — Do not use GitHub `tree/main` URLs in image `src`

This site intentionally uses `/assets/img/...` for the live image `src` values. A URL containing `github.com/.../tree/main/...` opens the GitHub file browser and is not a direct image file for a production website.

## Step 10 — Optional custom domain

No `CNAME` file is needed for `AIRLabHassen.github.io`. A `CNAME` file is only for a separate custom domain you own, such as `www.example.org`.
