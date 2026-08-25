# rvenvale-cdn
CDN image repository for [Rvenvale](https://github.com/nekowawolf/rvenvale).

This repository serves as the cloud storage and Content Delivery Network (CDN) via GitHub Pages for the Rvenvale image hosting platform.

## How it works

When you upload an image through the Rvenvale dashboard, the backend automatically converts the image to WebP format, pushes it to this repository, and serves it globally using GitHub Pages.

### Setup Instructions

1. **Enable GitHub Pages**: Go to **Settings** > **Pages** in this repository. Set the source to deploy from the `main` branch.
2. **Get your GitHub Token**: 
   - Go to your GitHub **Settings** > **Developer Settings** > **Personal Access Tokens (Tokens (classic))**.
   - Click **Generate new token (classic)**.
   - Give it a name (e.g., "Rvenvale CDN") and check the `repo` scope (this gives it permission to push images).
   - Copy the token and paste it into your Rvenvale `.env` file as `GITHUB_TOKEN`.
3. **No need to create folders manually!** 
   - You don't need to manually create an `images/` folder here. 
   - Rvenvale will automatically create the folder based on what you set in the `GITHUB_UPLOAD_DIR` variable in your `.env` file.
