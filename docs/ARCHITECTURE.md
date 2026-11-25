# Architecture

## Components

- **Test client:** controlled application or coding agent sending synthetic test prompts.
- **Egress inspection:** local checks and redaction before a request leaves the test boundary.
- **Route inventory:** records declared router, provider, model, endpoint, region and policy metadata.
- **Canary service:** issues unique opaque identifiers and receives controlled callbacks.
- **Event normaliser:** emits structured events with stable correlation IDs.
- **Evidence store:** retains minimal event data and experiment configuration.
- **Reporter:** creates a human-readable timeline and limitations statement.

## Trust boundaries

The local test harness, inference router, provider, downstream infrastructure and callback observer are separate trust domains. The framework must not imply visibility into infrastructure it cannot inspect.

## Event design

Events should be append-only where practical, timestamped in UTC, correlated to an experiment, and explicit about evidence source and confidence. Avoid storing raw prompts by default.
