# Adoption Guide

## Start a project

1. Create a repository from this template.
2. Replace placeholders in `PROJECT_STATUS.md` and `docs/PROJECT_OVERRIDES.md`.
3. Add architecture and development guidance for the technology stack.
4. Define phases in `docs/ROADMAP.md`.
5. Configure branch protection and required checks.
6. Adapt `.github/workflows/impact-validation.example.yml` to real project paths and commands, then rename it without `.example`.
7. Confirm the fallback for unknown paths runs full non-integration validation.
8. Create the first phase and WP issue.
9. Claim it before implementation.

## Required GitHub settings

- Protect the default branch.
- Require pull requests.
- Require the stable validation gate.
- Require current branches before merge.
- Prevent force pushes and branch deletion on protected branches.
- Enable automatic deletion of merged feature branches.
- Define who may change roadmap priority and promote RWPs.

## Project-specific decisions

Record these in `docs/PROJECT_OVERRIDES.md`:

- default branch
- technology and architecture boundaries
- commands for each affected area
- integration/external service test policy
- phase-closure criteria
- review authority
- deployment and rollback requirements
- security or compliance gates

## Keep the template neutral

Copy the process, not another product's application assumptions. Area mappings, test commands, stack rules, and release requirements belong in the adopting project.
