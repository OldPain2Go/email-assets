# OldPain2Go email-assets

Public static asset hosting for OldPain2Go email signature images, served via GitHub Pages at:

**`https://assets.oldpain2go.com/`**

## Why this exists

Email signature images need a stable, publicly-reachable URL so recipients see them inline (no broken icons, no "5 attachments" chips in Proton/Gmail). Hosting on a dedicated subdomain (vs the marketing website or a third-party CDN) means:

- URLs stay stable across website host migrations
- Brand-aligned URL in email source
- Free hosting via GitHub Pages with custom domain + Let's Encrypt SSL
- Foundation for future BIMI logo hosting

## Current assets

| File | Purpose | Used in |
|---|---|---|
| `op2go-cpd-badge.png` | OldPain2Go + CPD Accredited combined badge | Email signatures (all team members) |
| `facebook.png` | Facebook icon | Email signatures |
| `instagram.png` | Instagram icon | Email signatures |
| `linkedin.png` | LinkedIn icon | Email signatures |
| `youtube.png` | YouTube icon | Email signatures |

All images are pre-optimised PNGs (FastOctree quantisation) for minimal email size.

## Adding new assets

```bash
gh repo clone OldPain2Go/email-assets
cd email-assets
cp /path/to/new-asset.png .
git add new-asset.png
git commit -m "add: new-asset.png"
git push
# Live within ~1-2 min at https://assets.oldpain2go.com/new-asset.png
```

## Source / canonical

Original (pre-optimisation) signature images live in the OldPain2Go vault at:
`6. OldPain2Go/3 Resources/Brand Assets/Email Signatures/0 - Mailbox Signature (ACTIVE — uses variables)/FreeScout Optimised/images/`

This repo holds the **public-facing** copies with URL-safe filenames.

## Future use

- BIMI logo (when registered) — drop SVG Tiny PS file here, point DMARC `default._bimi` record at it
- Any future email-template imagery (product shots, banners, etc) for transactional emails
