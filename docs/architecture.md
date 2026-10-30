# Architecture

## Main boundaries

Entre Destinos separates editorial content, page templates, generated output, and runtime integrations.

```text
content + templates -> build and validation -> generated public website
                                              |
                                              +-> serverless integrations
```

The public build contains only assets required by the website. Test fixtures, publishing tools, private product files, and operational documentation stay outside the deployed output.

## Content layer

Page copy, navigation, media references, SEO fields, and blog articles are stored as structured content. This lets editors update the site without changing implementation files.

## Build layer

The Node.js build:

- Combines structured content with page templates
- Generates article and category routes
- Normalizes canonical URLs
- Creates redirects for supported legacy routes
- Produces sitemap and robots files
- Adds metadata, breadcrumbs, and structured data
- Validates links, images, and required content

## Editorial layer

Decap CMS is configured as a private, invitation-only interface. Editorial changes use a review workflow so generated output is produced only after an approved content change reaches the main branch.

## Runtime layer

Most pages are static. Runtime behavior is limited to the integrations that need it, including checkout, webhook processing, and form handling. Sensitive values are supplied by the hosting platform rather than committed to source control.

## Reliability decisions

- Build output never overwrites source content.
- External feeds have time limits and manual fallbacks.
- Internal links and generated routes are tested.
- Image dimensions and privacy metadata are handled during the build.
- Clean URLs, canonical tags, redirects, and sitemap routes share the same routing rules.

## Public showcase boundary

This repository explains the system but does not reproduce production source, private content, credentials, customer records, or paid files.
