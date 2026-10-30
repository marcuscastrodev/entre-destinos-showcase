<div align="center">

**🇺🇸 English** · [🇧🇷 Português](./README.pt-BR.md)

# Entre Destinos

### Content, travel services, and digital commerce in one publishing platform

**A product and engineering case study by Marcus Castro.**

[Live website](https://entredestinosmm.com/) · [Architecture](docs/architecture.md) · [Product capabilities](docs/features.md)

</div>

> **Public portfolio showcase.** The production source code, credentials, customer information, paid digital products, and operational configuration remain private. This repository documents the product, architecture, and engineering work without exposing sensitive assets.

## The project

Entre Destinos is a travel content and services platform that combines editorial publishing, lead generation, product checkout, and digital delivery. The public website is generated from structured content and deployed through a controlled editorial workflow.

The project brings together several journeys:

- Travel articles organized by category
- A Home Finder service for people planning an international move
- A digital kit for remote workers
- Newsletter acquisition and conversion pages
- Search-friendly content architecture
- A private editorial workspace for non-technical publishing

## What I built

### Static publishing system

Node.js build scripts combine page templates with structured JSON content and generate the deployable website. Generated output is isolated from source files, keeping editorial content and implementation concerns separate.

### Editorial workflow

Decap CMS provides an invitation-only publishing interface for pages, navigation, SEO fields, media, and blog articles. Editorial changes follow a review workflow before reaching the production branch.

### Search and content architecture

The build creates clean canonical URLs, article and category pages, redirects from legacy formats, breadcrumbs, sitemap entries, robots directives, metadata, and structured data for relevant page types.

### Commerce and digital delivery

The platform integrates Mercado Pago checkout with serverless functions and webhook-based delivery. Production credentials and the paid digital product are intentionally excluded from this showcase.

### Verification and privacy

Automated tests cover publishing behavior, internal links, media handling, structured data, page generation, editorial previews, and serverless flows. The image pipeline removes embedded metadata, including location-related EXIF fields, from published images.

## Engineering highlights

- Structured content separated from presentation templates
- Static generation for predictable delivery and performance
- Editorial previews and reviewed publishing workflows
- Blog, category, breadcrumb, canonical, redirect, and sitemap automation
- Schema.org structured data derived from visible site content
- Serverless checkout and webhook processing
- Graceful fallback for external content feeds
- Automated validation across content, SEO, media, and publishing flows
- Privacy-aware image processing

## Technology

| Area | Technologies |
| --- | --- |
| Build system | Node.js, JavaScript, custom static generation |
| Content | JSON, Markdown, Decap CMS |
| Hosting | Netlify, serverless functions, Git-based deployment |
| Commerce | Mercado Pago checkout and webhooks |
| Quality | Node test runner, automated content and build validation |
| Frontend | Semantic HTML, CSS, JavaScript, responsive layouts |

## Architecture at a glance

```text
Editors
   |
   v
Decap CMS + reviewed Git workflow
   |
   v
Structured page and article content
   |
   v
Node.js build and validation
   |
   +----> Generated pages, metadata, sitemap, redirects
   |
   v
Netlify deployment
   |
   +----> Public website
   +----> Serverless checkout and webhook flows
```

Read the [architecture notes](docs/architecture.md) for the main boundaries and decisions.

## My role

This project demonstrates work across:

- Product and information architecture
- Frontend implementation and responsive behavior
- Content modeling and editorial workflow design
- Static-site generation and build automation
- SEO foundations and structured data
- Checkout and webhook integration
- Testing, debugging, documentation, and deployment

## Screenshots

The [screenshot gallery](screenshots/README.md) is being prepared with reviewed public images. No administration screens, customer information, checkout credentials, or private product files will be published.

## Repository boundaries

This showcase does not distribute:

- Production application source
- Environment values, tokens, or account identifiers
- Customer or subscriber information
- The paid digital product
- Private CMS or infrastructure configuration

The live website and its content remain the authoritative public product experience.

---

**Built and documented by [Marcus Castro](https://github.com/marcuscastrodev)** · Web development, product thinking, and digital strategy
