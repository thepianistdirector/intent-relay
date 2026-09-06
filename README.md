# Intent Relay

**Preview, approve and recover AI-driven work across the tools your organization already uses.**

An agent can call five tools. Who makes sure the work still makes sense when the third call fails?

![Intent Relay: aspirational concept, not an implemented product](assets/vision-concept.png)

> This is a public planning repository. There is no product implementation or playable build yet. The image is an AI-generated vision reference, not a screenshot. All waves and tasks are proposed; no completed work, community approval or funding is implied.

## The mission

Build an open execution layer for consequential agent work across applications. Turn a proposed change into inspectable steps, narrow permissions, confirmed effects and a recovery plan that a person can understand.

Ask an agent to prepare a business change. Inspect what will change, approve the permitted steps, follow the actual results and recover a partial failure without guessing which actions happened.

## Who this is for

Developers and operations teams deploying agents into real multi-application workflows.

## The first thing we want to prove

A synthetic supplier-order workflow across inventory, reservation and draft-order services. Demonstrate previews, scoped approval, retries and partial failure recovery before connecting real customer systems.

External tools do not share a transaction manager. Universal rollback and universal exactly-once execution are not credible promises. Expose uncertainty and require reconciliation when a provider cannot prove an effect.

## What this could become

A shared library of connector contracts and recovery semantics that can work across models, agent frameworks and self-hosted business systems.

Tool protocols, durable workflows and governed enterprise agent products already exist. This proposal focuses on open, application-spanning effect descriptions and practical recovery, with honest distinctions between reversible, compensatable and irreversible operations.

## Why build it together

Domain experts and connector maintainers can contribute small effect contracts, fault fixtures and recovery recipes. Their shared knowledge is more valuable than another generic agent wrapper.

We are looking for founding maintainers and contributors who can make one small, reviewable part real. Bring a concrete use case, a difficult test case, an interface sketch or a focused patch. If you use a coding agent, give it one agreed task and review its result. Accepted work matters more than generated volume.

## Build the first useful piece with us

Start with [Intent Relay on Tanduna](https://tanduna.com/projects/intent-relay) and the [first task: Specify operation and approval contracts](https://tanduna.com/p/intent-relay/tasks/tsk_008dcae410ef951971030363f82adef9). Bring a concrete use case, a difficult fixture or time to review a small contribution. An agent can help do the work; a maintainer still checks that the result meets the agreed task.

1. Pick one task from the [six-wave roadmap](ROADMAP.md) and [twelve task contracts](TASKS.md), then agree its scope and prerequisites.
2. Read its exact repository/base, preferred model and fallback, required skills, testing procedure and acceptance flow.
3. Work on the accepted revision and return a focused patch or artifact with evidence another contributor can reproduce.

The first milestone is **Describe the effects before the calls**: Define a minimal contract around intent and consequences.

The complete [contribution guide](CONTRIBUTING.md) includes two public downloads: the [shared contribution skill](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Intent Relay validation skill](https://raw.githubusercontent.com/thepianistdirector/intent-relay/9710751a9ce5fdfe97cbcbed598075bf492c30df/.agents/skills/intent-relay-validation/SKILL.md). Both are pinned to exact Git commits. Every task selects GPT-6 Astra or Claude Fable 5.1 as preferred model and the other as fallback, with Medium or High effort stated explicitly.

This repository currently contains the proposal, concept art, roadmap, task contracts and contribution skills. It does not yet contain a working product. Future implementation tasks remain dependent on earlier results and a maintainer-approved execution baseline. The written contract describes what contributors must satisfy; it does not claim every corresponding Tanduna enforcement feature is already live.

## What we are not promising

No automatic production writes by default, credential pooling or pretending that sending a message can be undone. Connector access remains with its owner and each irreversible action needs an explicit policy.

There is no delivery date, token target, paid offer or crowdfunding campaign here. Community interest does not guarantee a finished product. The next milestone depends on contributors, maintainer capacity and evidence from the previous one.

## Existing work we should learn from

- [Model Context Protocol](https://modelcontextprotocol.io/docs/getting-started/intro)
- [Temporal](https://docs.temporal.io/)
- [ServiceNow Action Fabric](https://www.servicenow.com/platform/action-fabric.html)

These are related foundations and references, not partners or endorsements. We should reuse compatible components or contribute upstream when that is the better route. This proposal does not claim that its individual ingredients are unprecedented. Dependencies and their licenses will be evaluated before adoption.

## License and contribution

This repository is published under [GNU AGPL-3.0](LICENSE). See [CONTRIBUTING.md](CONTRIBUTING.md) for the proposed contribution workflow and [the image note](assets/README.md) for concept provenance.
