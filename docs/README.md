# Employ portal documentation dummy

This repository represents the small documentation workflow used to test the cross-repository deployment path.

## Trigger flow

1. A documentation change is pushed to `main`.
2. `.github/workflows/notify-docs-dummy.yml` runs on GitHub Actions.
3. The workflow sends a `documentation_updated` event to `Encryption-Consulting-LLC/docs-dummy`.
4. The target repository builds and deploys the staging documentation page.

The deployed verification page is available at `http://10.0.0.150` in the dummy staging environment.

## Required repository secret

Create `DOCS_DUMMY_DISPATCH_TOKEN` in this repository. It must be a narrowly scoped GitHub token or GitHub App credential that can dispatch workflows/events to `Encryption-Consulting-LLC/docs-dummy`. Do not place the token in YAML or commit it.

## Test change

This document is intentionally small. Editing it and pushing to `main` is enough to verify that the notification workflow triggers the main staging deployment workflow.
