# Gap and Remediation Process

## Issue first

Every new gap begins as a GitHub issue with:

- observed behavior and expected behavior
- reproducible evidence
- affected phase and packages
- user, architecture, security, and migration impact
- suggested urgency
- links to related code, PRs, and tests

Apply `gap-found`. Do not label it remediation until planning review.

## Planning classification

- **In-scope defect** — linked into the active package.
- **Backlog defect** — issue remains queued without roadmap rewrite.
- **RWP** — substantial historical, architectural, or cross-package correction.
- **Reconciliation** — adapts later completed work after remediation.
- **No action** — close with reasoning.

## RWP requirements

Use `RWP-<origin-phase>.<sequence>`. Define dependencies, queue position, migration/reconciliation impact, acceptance criteria, execution mode, and affected validation. Never renumber completed roadmap history.
