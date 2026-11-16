<p align="center"><img src="https://raw.githubusercontent.com/angelia-dev/.github/main/brand/angelia-logo-500.png" alt="Angelia logo: a capital A with a version-bump chevron and message waves" width="160"></p>

# Angelia

> *Angelia* (ἀγγελία): ancient Greek for "message, news".

**The self-hosted release event bus.** Angelia watches upstream artifacts (PyPI, npm, crates.io, GitHub/GitLab releases, OCI images, …), detects every new version, and delivers one clean, signed, machine-readable event ([CloudEvents](https://cloudevents.io)) to your CI, your chat, or your AI agents.

```
detect  ──▶  normalize  ──▶  deliver
(PyPI, npm,   (version parse,   (webhooks, GitHub dispatch,
 crates, GH,   semver delta,     chat, NATS, pull API,
 OCI, …)       filters, dedup)   SSE, MCP for agents)
```

What to *do* with a new version (open a PR, run tests, ask an agent) stays with the consumer. Angelia's job is to tell it, reliably and once.

**📖 Documentation: [angelia-dev.github.io/docs](https://angelia-dev.github.io/docs/)**: [quickstart](https://angelia-dev.github.io/docs/get-started/quickstart/), [watch sources](https://angelia-dev.github.io/docs/sources/), [notifications](https://angelia-dev.github.io/docs/notify/), [recipes](https://angelia-dev.github.io/docs/recipes/) and narrated [video tours](https://angelia-dev.github.io/docs/get-started/videos/).

## Repositories

| Repository | Purpose |
|---|---|
| [angelia](https://github.com/angelia-dev/angelia) | Core server, CLI, built-in sources and sinks. Design docs live here. |
| [spec](https://github.com/angelia-dev/spec) | Event schema (CloudEvents types, JSON Schema) and OpenAPI specification |
| [actions](https://github.com/angelia-dev/actions) | GitHub Actions to consume Angelia release events in workflows |
| [helm-charts](https://github.com/angelia-dev/helm-charts) | Helm charts to deploy Angelia on Kubernetes |
| [docs](https://github.com/angelia-dev/docs) | Website and documentation, published at [angelia-dev.github.io/docs](https://angelia-dev.github.io/docs/) |

## Status

**Pre-1.0, installable.** [v0.2.0](https://github.com/angelia-dev/angelia/releases/tag/v0.2.0) ships push delivery (webhooks, GitHub dispatch, chat), the REST and pull APIs, SSE, MCP and Postgres. Start with the [quickstart](https://angelia-dev.github.io/docs/get-started/quickstart/). Ideas and feedback are welcome in [Discussions](https://github.com/angelia-dev/angelia/discussions).

Licensed under Apache-2.0.
