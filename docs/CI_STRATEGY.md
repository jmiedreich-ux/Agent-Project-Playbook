# Impact-Based CI Strategy

## Ordinary WP/RWP

1. Detect changed paths.
2. Map them to affected components.
3. Build affected components and direct dependents.
4. Run explicitly affected non-integration unit-test projects.
5. Skip unrelated application, frontend, mobile, TV, and package checks.
6. Publish one stable required gate summarizing applicable jobs.

## Widening rules

Run broader validation for shared contracts/models, dependency injection, authentication, migrations, project/solution files, dependency manifests, workflow changes, and unknown paths.

## Full validation triggers

- phase closure
- nightly or manual full run
- workflow-policy change
- explicit `full-validation` label
- unknown-path conservative fallback

## Documentation-only changes

Run formatting, links, schemas, queue/status consistency, and template checks only. Do not build applications.

## Efficiency controls

- keep completion evidence in the implementation PR
- cancel superseded runs
- cache dependency restores safely
- use path filters and job outputs
- avoid duplicate post-merge validation
- retain full regression visibility through nightly and phase closure
