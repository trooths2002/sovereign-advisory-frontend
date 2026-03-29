# Security Policy

## Scope

This repository publishes static artifacts through GitHub Pages for controlled web delivery.

Security scope includes:
- `.github/workflows/pages.yml`
- GitHub Pages publish behavior
- repository contents on public branches
- staged HTML and CSS artifacts used for delivery

## Reporting

Do not open a public issue for:
- suspected secret exposure
- workflow abuse
- unauthorized content publication
- Pages misconfiguration with security impact

Use a private reporting path instead:
1. GitHub private vulnerability reporting, if enabled.
2. An existing private maintainer contact channel.

Do not include live secret values in a report.
If a credential may be exposed, rotate or revoke it first, then report the incident.

## Repository Rules

- Do not commit secrets, tokens, credentials, or production webhook URLs.
- Do not commit localhost, tunnel, or test webhook endpoints into public artifacts.
- GitHub Actions must be pinned to immutable commit SHAs.
- Only the minimum artifact set required for the Google Sites control/artifact layer may be published.
- Operator-only, staging-only, or diagnostic assets must not be exposed on the public Pages surface.

## Supported Hardening Baseline

The expected baseline for this repository is:
- SHA-pinned GitHub Actions
- scoped workflow permissions
- Dependabot enabled for GitHub Actions
- no public custom-domain binding unless explicitly required
- no unnecessary public staging artifacts
