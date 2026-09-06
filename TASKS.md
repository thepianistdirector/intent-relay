# Intent Relay: task contracts

Twelve proposed work packages, with named waves and dependency order. None is completed by publishing this document. The linked Tanduna revision is the contribution authority; this repository records the maintainer's intended contract while Tanduna's structured requirement support is being updated.

Every task below names its repository, branch, verified planning commit, preferred model, allowed fallback, immutable public skills, task-specific testing procedure and maintainer acceptance flow. A later implementation task still needs its prerequisite code, a rebased execution revision, narrow file scope and real functional commands. Do not treat the current planning commit as if that future code exists.

The allowed model pair is GPT-6 Astra and Claude Fable 5.1, with the effort stated per task. A model declaration is not independent runtime evidence; unresolved proof remains visible to the maintainer. See [CONTRIBUTING.md](CONTRIBUTING.md) and [the machine-readable authored contracts](task-contracts.json).

## W1-T1 — Specify operation and approval contracts

**Wave:** W1 · **Prerequisites:** None; maintainer scope review first

Model read, prepare, commit, reconcile and compensate where a provider supports them.

**Saved Tanduna task:** [W1-T1](https://tanduna.com/p/intent-relay/tasks/tsk_008dcae410ef951971030363f82adef9)

**Repository:** [https://github.com/thepianistdirector/intent-relay](https://github.com/thepianistdirector/intent-relay) · **Branch:** `main`

**Planning base commit:** [`9710751a9ce5fdfe97cbcbed598075bf492c30df`](https://github.com/thepianistdirector/intent-relay/commit/9710751a9ce5fdfe97cbcbed598075bf492c30df)

**Execution gate:** Maintainer accepts the scoped design protocol; this is not product implementation.

**Preferred:** `gpt-6-astra` / medium. **Accepted fallback:** `claude-fable-5-1` / medium. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Intent Relay validation](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Three example operations explicitly declare permissions and reversibility limits.
- An approval binds to the proposed arguments and becomes invalid when they change.

### Testing procedure

Trace a draft-order intent through preview, approval, execution and reconciliation. Change a precondition after preview and rehearse refusal or renewed approval; mark provider idempotency and compensation capabilities explicitly.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 9710751a9ce5fdfe97cbcbed598075bf492c30df
```

This task uses the saved reproducible manual protocol. Distinguish paper/synthetic exercises from actual participant or physical observations.

**Evidence artifact:** `docs/work/W1-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W1-T2 — Build a partial-failure scenario pack

**Wave:** W1 · **Prerequisites:** W1-T1

Describe retries, timeouts, ambiguous provider responses and human intervention.

**Saved Tanduna task:** [W1-T2](https://tanduna.com/p/intent-relay/tasks/tsk_d0ea047750c36faf8d7b78404875af08)

**Repository:** [https://github.com/thepianistdirector/intent-relay](https://github.com/thepianistdirector/intent-relay) · **Branch:** `main`

**Planning base commit:** [`9710751a9ce5fdfe97cbcbed598075bf492c30df`](https://github.com/thepianistdirector/intent-relay/commit/9710751a9ce5fdfe97cbcbed598075bf492c30df)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Intent Relay validation](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Each scenario states what is known, unknown and safe to try next.
- At least one scenario requires reconciliation rather than a claimed automatic rollback.

### Testing procedure

Build fixtures for timeout before send, success with lost response, duplicate delivery and changed external state. Specify the expected durable state and allowed next action for each case before implementation.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 9710751a9ce5fdfe97cbcbed598075bf492c30df
```

This task uses the saved reproducible manual protocol. Distinguish paper/synthetic exercises from actual participant or physical observations.

**Evidence artifact:** `docs/work/W1-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W2-T1 — Build the inventory-to-draft-order fixture

**Wave:** W2 · **Prerequisites:** W1-T1, W1-T2

Create synthetic inventory, reservation and order services with controllable failures.

**Saved Tanduna task:** [W2-T1](https://tanduna.com/p/intent-relay/tasks/tsk_a57880136cf04fc38caa968841283266)

**Repository:** [https://github.com/thepianistdirector/intent-relay](https://github.com/thepianistdirector/intent-relay) · **Branch:** `main`

**Planning base commit:** [`9710751a9ce5fdfe97cbcbed598075bf492c30df`](https://github.com/thepianistdirector/intent-relay/commit/9710751a9ce5fdfe97cbcbed598075bf492c30df)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Intent Relay validation](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- A complete run produces the intended final state across the fixture services.
- Each service can fail before and after applying an effect.

### Testing procedure

Run the inventory-to-draft-order fixture with sufficient and insufficient stock. Interrupt submission and retry; compare the final external draft and inventory references with the approved intent, with no real purchase.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 9710751a9ce5fdfe97cbcbed598075bf492c30df
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W2-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W2-T2 — Render a human-readable change preview

**Wave:** W2 · **Prerequisites:** W1-T1, W1-T2

Show proposed effects, scope, dependencies and approval requirements.

**Saved Tanduna task:** [W2-T2](https://tanduna.com/p/intent-relay/tasks/tsk_25345926856ba14a507a490724a50f2e)

**Repository:** [https://github.com/thepianistdirector/intent-relay](https://github.com/thepianistdirector/intent-relay) · **Branch:** `main`

**Planning base commit:** [`9710751a9ce5fdfe97cbcbed598075bf492c30df`](https://github.com/thepianistdirector/intent-relay/commit/9710751a9ce5fdfe97cbcbed598075bf492c30df)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `claude-fable-5-1` / high. **Accepted fallback:** `gpt-6-astra` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Intent Relay validation](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- A reviewer can identify which records would change before execution.
- A changed quantity or target invalidates the previous approval.

### Testing procedure

Ask a reviewer to explain affected records and consequences from the preview. Change the underlying record after preview, attempt approval and verify renewed review or refusal; repeat with keyboard-only interaction.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 9710751a9ce5fdfe97cbcbed598075bf492c30df
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W2-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W3-T1 — Implement durable execution and reconciliation

**Wave:** W3 · **Prerequisites:** W2-T1, W2-T2

Persist step state and recover after process or provider interruption.

**Saved Tanduna task:** [W3-T1](https://tanduna.com/p/intent-relay/tasks/tsk_498d90d9528a203ec550139dc13237e4)

**Repository:** [https://github.com/thepianistdirector/intent-relay](https://github.com/thepianistdirector/intent-relay) · **Branch:** `main`

**Planning base commit:** [`9710751a9ce5fdfe97cbcbed598075bf492c30df`](https://github.com/thepianistdirector/intent-relay/commit/9710751a9ce5fdfe97cbcbed598075bf492c30df)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Intent Relay validation](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Crash-and-retry scenarios do not silently duplicate supported idempotent effects.
- Ambiguous effects pause for evidence or review rather than being reported as successful.

### Testing procedure

Execute each partial-failure fixture and restart the worker between transitions. Reconcile durable state with the provider fixture; prove the claimed retry behavior and disclose operations without provider idempotency.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 9710751a9ce5fdfe97cbcbed598075bf492c30df
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W3-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W3-T2 — Implement bounded compensation paths

**Wave:** W3 · **Prerequisites:** W2-T1, W2-T2

Add explicit recovery for supported reversible or compensatable steps.

**Saved Tanduna task:** [W3-T2](https://tanduna.com/p/intent-relay/tasks/tsk_47bf55274241d86fa71f866a5ebead27)

**Repository:** [https://github.com/thepianistdirector/intent-relay](https://github.com/thepianistdirector/intent-relay) · **Branch:** `main`

**Planning base commit:** [`9710751a9ce5fdfe97cbcbed598075bf492c30df`](https://github.com/thepianistdirector/intent-relay/commit/9710751a9ce5fdfe97cbcbed598075bf492c30df)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Intent Relay validation](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- A failed reservation and partially prepared order recover according to their contracts.
- The system refuses to label an irreversible effect as rolled back.

### Testing procedure

Complete one supported compensable action and trigger recovery after partial success. Force compensation failure and an irreversible action; verify the record states the remaining effect and required human decision.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 9710751a9ce5fdfe97cbcbed598075bf492c30df
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W3-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W4-T1 — Publish a connector conformance kit

**Wave:** W4 · **Prerequisites:** W3-T1, W3-T2

Define fixtures for authorization, effect reporting, retry and recovery.

**Saved Tanduna task:** [W4-T1](https://tanduna.com/p/intent-relay/tasks/tsk_1169eeec09eee4180396c17ce230f9a3)

**Repository:** [https://github.com/thepianistdirector/intent-relay](https://github.com/thepianistdirector/intent-relay) · **Branch:** `main`

**Planning base commit:** [`9710751a9ce5fdfe97cbcbed598075bf492c30df`](https://github.com/thepianistdirector/intent-relay/commit/9710751a9ce5fdfe97cbcbed598075bf492c30df)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Intent Relay validation](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Two independent connector implementations pass the documented contract.
- A connector that falsely reports success is detected by a verification fixture.

### Testing procedure

Build a second connector against the documented operation contract. Exercise unsupported capability, duplicate request and ambiguous outcome cases; confirm conformance cannot pass from a connector's success string alone.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 9710751a9ce5fdfe97cbcbed598075bf492c30df
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W4-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W4-T2 — Pilot a low-risk real workflow

**Wave:** W4 · **Prerequisites:** W3-T1, W3-T2

Connect approved test accounts to a reversible workflow with narrow permissions.

**Saved Tanduna task:** [W4-T2](https://tanduna.com/p/intent-relay/tasks/tsk_dc7fff3cbd7c219ab6c2d90c1094c9f5)

**Repository:** [https://github.com/thepianistdirector/intent-relay](https://github.com/thepianistdirector/intent-relay) · **Branch:** `main`

**Planning base commit:** [`9710751a9ce5fdfe97cbcbed598075bf492c30df`](https://github.com/thepianistdirector/intent-relay/commit/9710751a9ce5fdfe97cbcbed598075bf492c30df)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Intent Relay validation](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- The owner can stop execution and inspect all resulting effects.
- Credentials and unrelated account data never appear in exported run records.

### Testing procedure

Use an explicitly approved low-risk test workflow and test account. Capture preview, owner approval, actual effect, reconciliation and recovery with one correlated record; stop before unapproved orders, messages or billing effects.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 9710751a9ce5fdfe97cbcbed598075bf492c30df
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W4-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W5-T1 — Add tenant and policy isolation

**Wave:** W5 · **Prerequisites:** W4-T1, W4-T2

Model per-team credentials, approval rules and run visibility.

**Saved Tanduna task:** [W5-T1](https://tanduna.com/p/intent-relay/tasks/tsk_ff9afc21a23470646901c5cca4e89905)

**Repository:** [https://github.com/thepianistdirector/intent-relay](https://github.com/thepianistdirector/intent-relay) · **Branch:** `main`

**Planning base commit:** [`9710751a9ce5fdfe97cbcbed598075bf492c30df`](https://github.com/thepianistdirector/intent-relay/commit/9710751a9ce5fdfe97cbcbed598075bf492c30df)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Intent Relay validation](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Cross-tenant reads and writes fail at execution and retrieval boundaries.
- Revoked access stops future steps and triggers an intelligible recovery state.

### Testing procedure

Run two synthetic tenants and policies against the same connector fixture. Attempt cross-tenant references and a policy-denied operation; inspect that neither executes or exposes the other tenant's data.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 9710751a9ce5fdfe97cbcbed598075bf492c30df
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W5-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W5-T2 — Integrate two agent runtimes

**Wave:** W5 · **Prerequisites:** W4-T1, W4-T2

Expose the same effect contract to two independently selected agent clients.

**Saved Tanduna task:** [W5-T2](https://tanduna.com/p/intent-relay/tasks/tsk_cd92f4ae1f8e78d0d738ba787b0b5151)

**Repository:** [https://github.com/thepianistdirector/intent-relay](https://github.com/thepianistdirector/intent-relay) · **Branch:** `main`

**Planning base commit:** [`9710751a9ce5fdfe97cbcbed598075bf492c30df`](https://github.com/thepianistdirector/intent-relay/commit/9710751a9ce5fdfe97cbcbed598075bf492c30df)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Intent Relay validation](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Both clients produce equivalent previews and follow the same approval boundary.
- The agent cannot override an operation's declared scope or recovery limits.

### Testing procedure

Submit the same intent from two supported agent runtimes. Verify both must pass the same approval and reconciliation contract; test a runtime attempting to skip preview or reuse stale approval.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 9710751a9ce5fdfe97cbcbed598075bf492c30df
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W5-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W6-T1 — Run failure and recovery drills

**Wave:** W6 · **Prerequisites:** W5-T1, W5-T2

Exercise process crashes, connector changes and missing provider receipts.

**Saved Tanduna task:** [W6-T1](https://tanduna.com/p/intent-relay/tasks/tsk_be42d1ad73d0a798987ac34d925d0ff0)

**Repository:** [https://github.com/thepianistdirector/intent-relay](https://github.com/thepianistdirector/intent-relay) · **Branch:** `main`

**Planning base commit:** [`9710751a9ce5fdfe97cbcbed598075bf492c30df`](https://github.com/thepianistdirector/intent-relay/commit/9710751a9ce5fdfe97cbcbed598075bf492c30df)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Intent Relay validation](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Publish reproducible recovery results and unresolved provider limitations.
- Operators can follow a written incident path without editing internal run state.

### Testing procedure

Rehearse the documented outage and recovery cases with fault timing retained. Compare intended, observed and unresolved effects after restart; include at least one case requiring manual reconciliation.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 9710751a9ce5fdfe97cbcbed598075bf492c30df
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W6-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W6-T2 — Publish the first supported connector catalog

**Wave:** W6 · **Prerequisites:** W5-T1, W5-T2

Document ownership, supported effects, maintenance and cost for a bounded catalog.

**Saved Tanduna task:** [W6-T2](https://tanduna.com/p/intent-relay/tasks/tsk_da4f2141c67d689dd3cb523650fb639a)

**Repository:** [https://github.com/thepianistdirector/intent-relay](https://github.com/thepianistdirector/intent-relay) · **Branch:** `main`

**Planning base commit:** [`9710751a9ce5fdfe97cbcbed598075bf492c30df`](https://github.com/thepianistdirector/intent-relay/commit/9710751a9ce5fdfe97cbcbed598075bf492c30df)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Intent Relay validation](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Each connector has a maintainer and reproducible compatibility evidence.
- Unsupported operations remain explicitly unavailable instead of falling back to unrestricted tool calls.

### Testing procedure

Install the catalog's supported connector versions in a clean fixture and run their conformance cases. Change one incompatible capability and verify the catalog reports the failure and last supported range.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 9710751a9ce5fdfe97cbcbed598075bf492c30df
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W6-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.
