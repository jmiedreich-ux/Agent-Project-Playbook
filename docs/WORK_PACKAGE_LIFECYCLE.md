# Work Package Lifecycle

1. **Discover** — record need or finding as a GitHub issue.
2. **Classify** — planning decides WP, in-scope defect, RWP, or no action.
3. **Approve** — define scope, acceptance criteria, dependencies, queue position, validation, and execution mode.
4. **Claim** — update `tracker/assignments.json` with owner, issue, branch, mode, and lanes.
5. **Implement** — stay inside approved scope.
6. **Validate** — run affected-area checks; widen for cross-cutting change.
7. **Review** — inspect exact-head diff, checks, feedback, security, architecture, and records.
8. **Complete** — include evidence in the implementation PR when practical.
9. **Merge** — merge only after required checks and approval.
10. **Release** — clear the claim, synchronize status/handoff, and identify one exact next action.

## Completion evidence

Record:

- issue, branch, PR, and head SHA
- acceptance criteria result
- affected checks and results
- intentionally skipped checks
- review decision
- migration/deployment notes
- residual risks
- merge commit
