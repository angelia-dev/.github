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

## Repositories

| Repository | Purpose |
|---|---|
| [angelia](https://github.com/angelia-dev/angelia) | Core server, CLI, built-in sources and sinks. Design docs live here. |
| [spec](https://github.com/angelia-dev/spec) | Event schema (CloudEvents types, JSON Schema) and OpenAPI specification |
| [actions](https://github.com/angelia-dev/actions) | GitHub Actions to consume Angelia release events in workflows |
| [helm-charts](https://github.com/angelia-dev/helm-charts) | Helm charts to deploy Angelia on Kubernetes |
| [docs](https://github.com/angelia-dev/docs) | Website and documentation |

## Status

**Pre-alpha / Phase 0.** Nothing is usable yet; we are validating the design. Ideas and feedback are welcome in [Discussions](https://github.com/angelia-dev/angelia/discussions).

Licensed under Apache-2.0.
