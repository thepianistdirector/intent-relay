# Intent Relay: proposed work packages

These are planning briefs. No task is complete or approved for automatic execution. Before implementation, maintainers must publish a scoped task revision with the actual repository, paths, tools and validation commands.

## W1-T1 — Specify operation and approval contracts

**Wave:** W1 · **Status:** Planned · **Prerequisites:** None; begin with maintainer scope review

Model read, prepare, commit, reconcile and compensate where a provider supports them.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Three example operations explicitly declare permissions and reversibility limits.
- An approval binds to the proposed arguments and becomes invalid when they change.

## W1-T2 — Build a partial-failure scenario pack

**Wave:** W1 · **Status:** Planned · **Prerequisites:** W1-T1

Describe retries, timeouts, ambiguous provider responses and human intervention.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Each scenario states what is known, unknown and safe to try next.
- At least one scenario requires reconciliation rather than a claimed automatic rollback.

## W2-T1 — Build the inventory-to-draft-order fixture

**Wave:** W2 · **Status:** Planned · **Prerequisites:** W1-T1, W1-T2

Create synthetic inventory, reservation and order services with controllable failures.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- A complete run produces the intended final state across the fixture services.
- Each service can fail before and after applying an effect.

## W2-T2 — Render a human-readable change preview

**Wave:** W2 · **Status:** Planned · **Prerequisites:** W1-T1, W1-T2

Show proposed effects, scope, dependencies and approval requirements.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- A reviewer can identify which records would change before execution.
- A changed quantity or target invalidates the previous approval.

## W3-T1 — Implement durable execution and reconciliation

**Wave:** W3 · **Status:** Planned · **Prerequisites:** W2-T1, W2-T2

Persist step state and recover after process or provider interruption.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Crash-and-retry scenarios do not silently duplicate supported idempotent effects.
- Ambiguous effects pause for evidence or review rather than being reported as successful.

## W3-T2 — Implement bounded compensation paths

**Wave:** W3 · **Status:** Planned · **Prerequisites:** W2-T1, W2-T2

Add explicit recovery for supported reversible or compensatable steps.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- A failed reservation and partially prepared order recover according to their contracts.
- The system refuses to label an irreversible effect as rolled back.

## W4-T1 — Publish a connector conformance kit

**Wave:** W4 · **Status:** Planned · **Prerequisites:** W3-T1, W3-T2

Define fixtures for authorization, effect reporting, retry and recovery.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Two independent connector implementations pass the documented contract.
- A connector that falsely reports success is detected by a verification fixture.

## W4-T2 — Pilot a low-risk real workflow

**Wave:** W4 · **Status:** Planned · **Prerequisites:** W3-T1, W3-T2

Connect approved test accounts to a reversible workflow with narrow permissions.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- The owner can stop execution and inspect all resulting effects.
- Credentials and unrelated account data never appear in exported run records.

## W5-T1 — Add tenant and policy isolation

**Wave:** W5 · **Status:** Planned · **Prerequisites:** W4-T1, W4-T2

Model per-team credentials, approval rules and run visibility.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Cross-tenant reads and writes fail at execution and retrieval boundaries.
- Revoked access stops future steps and triggers an intelligible recovery state.

## W5-T2 — Integrate two agent runtimes

**Wave:** W5 · **Status:** Planned · **Prerequisites:** W4-T1, W4-T2

Expose the same effect contract to two independently selected agent clients.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Both clients produce equivalent previews and follow the same approval boundary.
- The agent cannot override an operation's declared scope or recovery limits.

## W6-T1 — Run failure and recovery drills

**Wave:** W6 · **Status:** Planned · **Prerequisites:** W5-T1, W5-T2

Exercise process crashes, connector changes and missing provider receipts.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Publish reproducible recovery results and unresolved provider limitations.
- Operators can follow a written incident path without editing internal run state.

## W6-T2 — Publish the first supported connector catalog

**Wave:** W6 · **Status:** Planned · **Prerequisites:** W5-T1, W5-T2

Document ownership, supported effects, maintenance and cost for a bounded catalog.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Each connector has a maintainer and reproducible compatibility evidence.
- Unsupported operations remain explicitly unavailable instead of falling back to unrestricted tool calls.
