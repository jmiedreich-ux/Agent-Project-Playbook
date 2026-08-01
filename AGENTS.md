# Agent Project Rules

## Source of truth

Repository and GitHub state are authoritative. Chat history is supporting context only.

Before changing anything, read in order:

1. `AGENTS.md`
2. `ai/handoffs/current.md`
3. `PROJECT_STATUS.md`
4. `tracker/assignments.json`
5. The approved WP/RWP
6. Linked issue, branch, PR, and CI state
7. Project-specific architecture and development guidance

## Work authorization

- Every implementation or documentation change maps to one approved GitHub issue and one WP or RWP.
- Claim the item in `tracker/assignments.json` before editing.
- One WP/RWP uses one branch and one PR unless an approved package documents an inseparable exception.
- Normal branches: `wp/<id>-<name>`; remediation branches: `rwp/<id>-<name>`.
- Commit messages begin with the WP/RWP ID.
- Never start unrelated work from a testing or review finding.

## WP and RWP

- WP means planned roadmap work.
- Findings start as issues labeled `gap-found`.
- Testing/review agents may gather evidence but may not create, renumber, reprioritize, or insert WPs/RWPs.
- Small in-scope defects may remain in the active package only when the issue and package record link that decision.
- Substantial historical, architectural, or cross-package gaps require planning review and promotion to RWP.
- RWP IDs use `RWP-<origin-phase>.<sequence>`; completed WP history is never renumbered.
- Only the designated planning owner may promote RWPs or change queue order.
- If remediation alters a surface used by later completed work, schedule reconciliation before dependent roadmap work resumes.

## Execution modes

Every WP/RWP declares exactly one mode.

### Sequential

- Claim one approved WP/RWP.
- Complete, review, merge, and release it.
- Only then claim the next queue item.
- Stop when another owner already holds the next claim.

### Collaborative

- One orchestrator owns one WP/RWP claim.
- Agents receive explicit, non-overlapping lanes with writable, read-only, and prohibited files.
- Lane agents never claim separate roadmap work.
- Shared contracts, project files, dependency injection, migrations, workflows, trackers, and handoffs are orchestrator-owned.
- No two active agents edit the same file.
- Unexpected overlap requires stopping and re-planning.
- Only the orchestrator integrates lanes and prepares review.

## Validation

- GitHub Actions is authoritative.
- Ordinary WP/RWP PRs build affected areas and run explicitly affected non-integration unit tests only.
- Do not run the complete unit suite or unrelated frontend/TV/mobile packages by default.
- Widen validation for shared contracts, shared models, migrations, authentication, dependency injection, project files, package manifests, or other cross-cutting changes.
- Full non-integration validation is reserved for phase closure, nightly/manual execution, workflow changes, an explicit `full-validation` label, or conservative fallback for unknown paths.
- Documentation-only changes use lightweight record validation.
- Record intentionally skipped or non-applicable checks.
- Projects must define their own policy for integration/external-provider tests in `docs/PROJECT_OVERRIDES.md`.

## Review and completion

A WP/RWP is complete only when:

1. Acceptance criteria are satisfied.
2. Required checks pass on the exact PR head.
3. The full diff and unresolved feedback are reviewed.
4. Approval is recorded against that head.
5. Completion evidence is included in the implementation PR when practical.
6. Status, assignment tracker, active handoff, and immutable archive handoff agree.
7. The PR merges and the claim is released.

A new commit invalidates prior CI evidence and approval.

## Safety and scope

- Never commit secrets, credentials, machine-specific configuration, generated runtime output, or unrelated changes.
- Do not invent contracts, database fields, routes, events, or payloads.
- Do not refactor unrelated code.
- Stop and create an issue when work exceeds the approved scope.
