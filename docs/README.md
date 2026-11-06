# Employ portal documentation dummy

This repository represents the smaller documentation workflow. A push to its `main` branch runs `.github/workflows/notify-docs-dummy.yml`, which sends a `documentation_updated` event to `Encryption-Consulting-LLC/docs-dummy`.

The target repository then runs its normal staging build, package, deployment, health check, and rollback flow.

## Required repository secret

Create `DOCS_DUMMY_DISPATCH_TOKEN` in this repository. It must be a narrowly scoped GitHub token or GitHub App credential that can dispatch workflows/events to `Encryption-Consulting-LLC/docs-dummy`. Do not place the token in YAML or commit it.
