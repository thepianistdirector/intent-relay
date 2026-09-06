# Contributing to Intent Relay

Start with [the project on Tanduna](https://tanduna.com/projects/intent-relay) and select one [saved task](TASKS.md). Discuss your intended result before starting overlapping work. GitHub holds source and reviewable patches; Tanduna holds the community's task revisions and decisions.

## Before your agent starts

Use the exact repository, base commit and task revision in the accepted brief. The current planning baseline is `main` at `9710751a9ce5fdfe97cbcbed598075bf492c30df`. Later tasks must be rebound to the real integrated prerequisite code. Do not silently substitute current HEAD, invent a missing harness or treat a branch name as an immutable base.

Read both public, standalone skills:

1. [Tanduna contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md).
2. [Intent Relay validation](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md).

The links are pinned to Git commits and require no account. Save each as `SKILL.md` in the matching named skill folder used by your agent, or ask your agent to read the linked Markdown directly. Reading does not require installing or executing a downloaded script. These skills are covered by the hosting repositories' AGPL-3.0 licenses.

The preferred model and explicit fallback are listed for every task. Lucas permits GPT-6 Astra and Claude Fable 5.1 as mutual fallbacks for these tasks, using the specified Medium or High effort. Do not substitute another model or lower effort without a new maintainer decision. Record model/effort information exposed by the actual runtime, and clearly mark any contributor-only declaration or unavailable proof.

## Execute and request acceptance

Work in an isolated branch or fork with the saved allowed/excluded paths. Follow that task's testing procedure; keep failed and unrun checks visible. Design and playtest tasks use a reproducible manual protocol. Implementation tasks need real functional checks in the chosen stack plus runtime evidence. The baseline Git commands check identity and patch hygiene, not product behavior.

Submit the scoped patch or artifact, task ID/revision, base and result references, skill versions, model evidence and a criterion-by-criterion result report. The maintainer reviews and reproduces the relevant evidence before recording acceptance. Missing skills, a non-permitted model, unresolved required evidence or failed criteria cannot be converted into a passing contribution by self-reporting success.

If a prerequisite, scope, baseline or validation procedure is missing, explain the concrete gap and request a revised task before execution. Do not erase old task or review history. Changing execution instructions requires renewed review of the affected revision.

## Contribution boundaries

Keep credentials and private data out of prompts, artifacts and commits. Label generated concepts, simulated results, actual observations and unrun checks accurately. A planning task does not authorize purchases, account changes, live messages, merge or deployment.

Contribute material you have the right to publish under [AGPL-3.0](LICENSE), with attribution and third-party license records. Initial stewardship remains with the repository owner while founding maintainers are recruited. Accepted contributions matter; tokens spent do not automatically confer control, equity or voting rights.
