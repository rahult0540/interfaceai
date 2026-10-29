# Interface AI

**Any Source. Any Format. Any Destination.**

Interface AI is an early-stage initiative building domain-independent data migration and transformation technology. The goal is to ingest data from one system, map and transform it, validate the results, and deliver it in the format required by another system.

## Website

The public-facing website is in [index.html](index.html). It is a standalone, responsive HTML page with inline styling, JavaScript and an inline SVG logo. Open it locally in a browser to preview.

## Team quick start

```sh
git clone https://github.com/rahult0540/interfaceai.git
cd interfaceai
git switch -c feature/short-description
```

Open `index.html` in your browser; no dependencies or build step are required. This repository currently contains the website and product documentation. The FastAPI proof of concept described below is not included here.

Before making your first change, follow [CONTRIBUTING.md](CONTRIBUTING.md). Repository owners should also read [docs/TEAM_SETUP.md](docs/TEAM_SETUP.md) for branch protection and access guidance.

## Our initial products

| Product | Focus | Status |
| --- | --- | --- |
| Interface Data | System-to-system structured data migration, starting with life insurance policies | Early CSV-to-JSON prototype |
| Interface Knowledge | Employee and team knowledge portability across work tools | Planned |
| Interface Illustrate | Life insurance illustration, rider and benefit comparisons | Planned |

The platform vision is industry-agnostic. Insurance is an initial use case, **not** the overall scope.

## How migration works

1. **Ingest** source datasets from exports, files or integrations.
2. **Map** source fields to the destination data model.
3. **Transform and validate** records; flag exceptions for review.
4. **Deliver** the required target format or integrate with the destination.

## Technical approach

The initial life-insurance proof of concept uses FastAPI, CSV ingestion, deterministic mapping rules, validation, and canonical JSON output. It is not production-ready; it does not yet include live source/destination connectors, enterprise authentication, or real AI-driven mapping.

See [docs/PRODUCT_VISION.md](docs/PRODUCT_VISION.md) and [docs/DEPLOYMENT.md](docs/DEPLOYMENT.md).

## Hosting on Hostinger

Upload the root `index.html` into the domain's `public_html` directory using Hostinger hPanel File Manager. See deployment documentation for details.

## Contact

The website currently references `hello@interfaceai.io`. Confirm this mailbox is active before publishing.

## Disclaimer

Product names and brand assets are working concepts. Trademark clearance and production readiness have not been established.
