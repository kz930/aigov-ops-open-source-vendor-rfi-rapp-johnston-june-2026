# Safe-RFI Deployment

Safe-RFI is deployed as a static GitHub Pages site from this repository.

## Publishing model

- The GitHub Actions workflow `.github/workflows/deploy-pages.yml` runs on pushes to `main` and on manual dispatch.
- Workflow artifacts are built by copying `webapp/` content into a Pages artifact directory.
- `actions/deploy-pages` publishes the resulting static site.

## Local review

Because Safe-RFI is static HTML/CSS/JS, you can review by opening files directly in a browser:

- `index.html` for repository landing page
- `webapp/index.html` for the application

## Operational expectations

- Keep web assets self-contained and repository local.
- Avoid server-side assumptions.
- Keep links relative for compatibility with GitHub Pages paths.
