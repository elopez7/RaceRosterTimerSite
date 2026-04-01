# Project Site Template

A single-page landing site template for showcasing portfolio projects. No build tools or frameworks needed — just edit a config block and deploy.

## Quick Start

1. **Copy** this folder for your new project
2. **Edit** the `site` config block at the top of `index.html`:
   - `name` — your project name
   - `headline` — hero heading (supports HTML, wrap keywords in `<span class='highlight'>`)
   - `description` — one-liner shown below the headline
   - `appUrl` — link to your live app (set to `""` to hide the button)
   - `repoUrl` — GitHub repository URL
   - `features` — array of features, each with icon, title, description, and screenshot path
3. **Add images** to the `images/` folder:
   - `logo.svg` — your project logo (shown in nav)
   - One screenshot per feature (referenced in the config)
4. **Optional: Change the theme** — uncomment the `theme` object in the config and adjust colors:
   ```js
   theme: {
     "--accent": "#22c55e",
     "--accent-hover": "#4ade80",
     "--bg-primary": "#0a0a0a",
   },
   ```
5. **Deploy** — push to a repo connected to Netlify. The included `netlify.toml` handles the rest.

## File Structure

```
project-site-template/
  index.html      <- The entire site (edit the config block at the top)
  netlify.toml    <- Netlify deploy config
  .gitignore
  images/         <- Logo + feature screenshots
    logo.svg
    feature1.png
    feature2.png
    ...
  app/            <- Optional: your live app files (WASM, etc.)
```

## Preview Locally

```sh
python -m http.server 8080
# Open http://localhost:8080
```
