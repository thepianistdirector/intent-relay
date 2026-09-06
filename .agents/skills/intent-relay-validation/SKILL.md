---
name: intent-relay-validation
description: Validate a scoped Intent Relay contribution using its domain invariants and reproducible evidence; apply the checks relevant to the saved task.
---

# Validate approved effects and recovery

Read the exact task revision and select the checks that address its acceptance criteria. This skill does not expand a task to the entire roadmap or authorize future implementation. These are validation instructions, not claims of an existing product.

1. Represent each operation with its intended effect, precondition, approval boundary and provider capability. Compare the preview with the exact effect submitted after approval; stale approval must be reconsidered.

2. Use the inventory-to-draft-order fixture before a real workflow. Exercise timeout before submission, timeout after provider success, duplicate delivery and changed provider state.

3. Distinguish retry-safe operations, provider idempotency support, reconciliation and compensation. Never infer universal exactly-once execution from a local request ID.

4. For compensation, show what is reversible, what needs another approved action and what cannot be undone. Preserve an inspectable record of partial success and failed recovery.

5. Connector tests use isolated synthetic or explicitly approved test accounts. No real orders, messages or billing changes are authorized by a local test plan. Integration with two runtimes must preserve the same approval contract.

For every selected check, record fixture/setup, actions, expected outcome, observed outcome and reproducible evidence. State which checks were not applicable and why; do not count unrun checks as passing.
