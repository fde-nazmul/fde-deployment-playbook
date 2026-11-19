# Phase 2 — Scope

**Goal:** the smallest deployment that moves the success metric within 2–4 weeks.

## Do
- Cut to one workflow, one user group, one channel.
- Decide the autonomy level for each action: *suggest* → *draft for approval* → *act and report*.
- Set a hard monthly budget for model and infra spend.
- Write down what is explicitly **out** of scope.

## Risk register (minimum)
| Risk | Mitigation |
|---|---|
| Model output is wrong or off-brand | Human approval queue; deterministic fallback |
| Data leaves the client's control | Least-privilege keys; no training on client data; logs redacted |
| Cost spike | Per-day budget cap and alert |
| Vendor/API outage | Graceful degradation; retry with backoff; manual path documented |

## Output
A one-page scope (see [template](../templates/scope-one-pager.md)) signed off by the client.
