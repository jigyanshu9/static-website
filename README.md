# Static Website on GitHub Pages

A simple static website built with plain HTML and CSS and hosted for free on GitHub Pages. I made it as a hands-on DevOps exercise to practice taking code from a local machine to a live URL.

**Live website:** https://jigyanshu9.github.io/static-website/
**Repository:** https://github.com/jigyanshu9/static-website

## Objective

Deploy a simple HTML website using GitHub Pages and share a live link along with the GitHub repo.

## Tools used

- HTML and CSS
- Git and GitHub
- GitHub Pages

## Project structure

```
static-website/
├── index.html    # Page content and structure
├── style.css     # Styling (colors, typography, layout)
└── README.md     # Project documentation
```

## How it was deployed

1. Created `index.html` and `style.css` locally.
2. Created a new public repository named `static-website` on GitHub.
3. Pushed the files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Add static site"
   git branch -M main
   git remote add origin https://github.com/jigyanshu9/static-website.git
   git push -u origin main
   ```
4. Opened **Settings → Pages** in the repository.
5. Set the source to **Deploy from a branch**, selected the **main** branch and the **/ (root)** folder, and saved.
6. Waited for the deployment to finish (visible in the **Actions** tab) and opened the live link GitHub provided.

## Customizing with CSS

All colors are defined as variables at the top of `style.css`:

```css
:root {
  --bg: #eef2f5;      /* page background */
  --ink: #14213d;     /* main text color */
  --muted: #4a5a73;   /* secondary text */
  --accent: #0f766e;  /* buttons and highlights */
}
```

Change these values to restyle the whole site, then commit and push. GitHub Pages redeploys automatically after every push to `main`.

## Run it locally

No build step is needed. Clone the repo and open `index.html` in a browser:

```bash
git clone https://github.com/jigyanshu9/static-website.git
cd static-website
```

## Troubleshooting

- **404 error on the live link:** make sure the file is named `index.html` (lowercase) and sits at the repo root.
- **Page loads without styling:** check that `style.css` is in the same folder as `index.html`.
- **Changes not showing:** wait a minute for the deploy to finish, then hard refresh with Ctrl+Shift+R.

## Author

Jigyanshu ([@jigyanshu9](https://github.com/jigyanshu9))
