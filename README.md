# Agent Project Playbook

A technology-neutral GitHub template for running software projects with AI agents using governed work packages, remediation packages, explicit ownership, focused validation, and auditable completion.

The complete playbook is being introduced through the initial setup pull request.

## Core model

- **WP** — planned roadmap work
- **RWP** — approved remediation for a discovered historical or architectural gap
- **Sequential mode** — one agent claims and completes one WP/RWP at a time
- **Collaborative mode** — one orchestrator owns one WP/RWP while agents work in non-overlapping lanes
- **Issue first** — findings begin as issues; only planning promotes substantial gaps to RWPs
- **Impact-based CI** — ordinary WP/RWP changes build and test affected areas only
- **Full validation** — reserved for phase closure, nightly/manual runs, workflow changes, or explicit escalation

See `docs/ADOPTION_GUIDE.md` after the setup pull request is merged.
