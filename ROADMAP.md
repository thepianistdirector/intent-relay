# Intent Relay roadmap

This is a public planning repository. There is no product implementation or playable build yet. The image is an AI-generated vision reference, not a screenshot. All waves and tasks are proposed; no completed work, community approval or funding is implied.

The order reflects dependencies, not calendar commitments. Each wave advances only when its stated outcome is demonstrated and a maintainer accepts the next scope. Capacity targets are hypotheses to test.

## W1 — Describe the effects before the calls

Define a minimal contract around intent and consequences.

- **W1-T1: Specify operation and approval contracts.** Model read, prepare, commit, reconcile and compensate where a provider supports them.
- **W1-T2: Build a partial-failure scenario pack.** Describe retries, timeouts, ambiguous provider responses and human intervention.

## W2 — A synthetic workflow with real semantics

Implement the smallest inspectable multi-service run.

- **W2-T1: Build the inventory-to-draft-order fixture.** Create synthetic inventory, reservation and order services with controllable failures.
- **W2-T2: Render a human-readable change preview.** Show proposed effects, scope, dependencies and approval requirements.

## W3 — Execution that admits uncertainty

Handle failures without duplicating effects.

- **W3-T1: Implement durable execution and reconciliation.** Persist step state and recover after process or provider interruption.
- **W3-T2: Implement bounded compensation paths.** Add explicit recovery for supported reversible or compensatable steps.

## W4 — Connect real tools deliberately

Prove interoperability and ownership boundaries.

- **W4-T1: Publish a connector conformance kit.** Define fixtures for authorization, effect reporting, retry and recovery.
- **W4-T2: Pilot a low-risk real workflow.** Connect approved test accounts to a reversible workflow with narrow permissions.

## W5 — Work across teams and frameworks

Keep permissions and meaning stable as adoption grows.

- **W5-T1: Add tenant and policy isolation.** Model per-team credentials, approval rules and run visibility.
- **W5-T2: Integrate two agent runtimes.** Expose the same effect contract to two independently selected agent clients.

## W6 — An open recovery commons

Make operational reliability a maintained community asset.

- **W6-T1: Run failure and recovery drills.** Exercise process crashes, connector changes and missing provider receipts.
- **W6-T2: Publish the first supported connector catalog.** Document ownership, supported effects, maintenance and cost for a bounded catalog.

See [TASKS.md](TASKS.md) for observable acceptance criteria.
