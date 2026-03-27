# Everberry Events

Cultivating Connections — [www.everberryevents.com](https://www.everberryevents.com)

The site is currently displaying a "Coming Soon" landing page while the full website is under construction.

## Tech Stack

- **Jekyll 4.3** — static site generator
- **GitHub Pages** — hosting, deployed via GitHub Actions
- **Cloudflare** — DNS management
- **GoatCounter** — privacy-friendly analytics

## Project Structure

```
├── _config.yml                 # Jekyll configuration
├── _data/
│   └── contact.yml             # Contact details (email, phone, Instagram)
├── _layouts/
│   └── coming-soon.html        # Self-contained landing page layout
├── images/
│   └── everberryevents/logo/   # Brand logos
├── .github/workflows/
│   └── jekyll.yml              # GitHub Actions deploy workflow
├── index.md                    # Site entry point
├── CNAME                       # Custom domain config
├── Gemfile                     # Ruby dependencies
└── LICENSE
```

## Local Development

```bash
bundle install
bundle exec jekyll serve
```

## Deployment

Pushes to `main` trigger the GitHub Actions workflow which builds and deploys to GitHub Pages automatically.

## DNS

- Apex domain (`everberryevents.com`) — A records pointing to GitHub Pages IPs
- `www` subdomain — CNAME to `everberry.github.io`
- GitHub Pages handles the apex → www redirect and SSL via Let's Encrypt
- Cloudflare DNS records must be set to DNS only (grey cloud) for GitHub to provision and renew certificates

## SEO

The coming soon page includes Open Graph tags, Twitter Card meta, a canonical URL, and Organization structured data (JSON-LD).

## Analytics

Tracking via [GoatCounter](https://everberryevents.goatcounter.com) — a lightweight, privacy-friendly alternative to Google Analytics.
