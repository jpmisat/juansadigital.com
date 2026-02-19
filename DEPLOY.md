# Deploying JuansaDigital to Cloudflare Pages (GitHub Actions)

This guide walks you through deploying the Astro site to Cloudflare Pages using GitHub Actions.

## Prerequisites
- A Cloudflare account.
- The project pushed to a GitHub repository.
- A Cloudflare API Token.

## Setup Instructions

### 1. Generate API Token (Cloudflare)
1.  Log in to the [Cloudflare Dashboard](https://dash.cloudflare.com/).
2.  Go to **My Profile** > **API Tokens**.
3.  Create a token using the **Edit Cloudflare Workers** template.
4.  Copy the generated token.

### 2. Get Account ID (Cloudflare)
1.  Go to **Workers & Pages** in the dashboard.
2.  Copy your **Account ID** from the sidebar ("Account details").

### 3. Add GitHub Secrets (GitHub)
1.  Go to your GitHub repository > **Settings** > **Secrets and variables** > **Actions**.
2.  Add the following secrets:
    - `CLOUDFLARE_API_TOKEN`: Your API token from step 1.
    - `CLOUDFLARE_ACCOUNT_ID`: Your Account ID from step 2.

> **Note**: You do NOT need to create `GITHUB_TOKEN`. GitHub creates this automatically for every workflow run.

### 4. Deploy
- Simply push changes to the `main` branch.
- The GitHub Action will automatically:
    1.  Create the project `juansadigital-astro` in Cloudflare if it doesn't exist.
    2.  Assign the custom domain `juansa.connexis.co`.
    3.  Build your site.
    4.  Deploy it to Cloudflare Pages.

> **Important**: For the custom domain `juansa.connexis.co` to work, ensuring your DNS records point to Cloudflare is usually required, but Cloudflare Pages often handles the CNAME validation if the domain is on Cloudflare. If not, follow instructions in Cloudflare Dashboard > Pages > Custom Domains if verification is needed.
