# Agent Modes

## Sequential mode

Use when work cannot be divided safely or for scheduled automation.

- One active claim.
- One WP/RWP at a time.
- Queue order is mandatory.
- A conflicting claim stops the later agent.
- Release ownership only after merge and synchronized records.

## Collaborative mode

Use when one package contains independent lanes.

Before work begins, document:

| Lane | Owner | Writable | Read-only | Prohibited | Deliverable |
|---|---|---|---|---|---|

The orchestrator owns shared files, integration, tracker changes, handoffs, PR preparation, and conflict resolution. Lanes do not create separate WP/RWP claims.

## Mode changes

Changing mode requires updating the approved package, issue, tracker, and handoff. It never bypasses normal issue, branch, PR, validation, or approval gates.
