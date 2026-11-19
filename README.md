# FDE Deployment Playbook

**How I take an AI system from "interesting demo" to "running in a client's business" — the Forward Deployed Engineer way.**

A Forward Deployed Engineer sits between the customer and the product. The job is to understand the customer's real workflow, ship something that works inside it, and feed what you learn back into the product. This playbook is the process I use with B2B clients at [ZeekWeb](https://zeekweb.com): exporters, manufacturers and SMEs adopting AI agents, SEO/GEO automation and lead generation.

## The 5 phases

| # | Phase | Goal | Exit criteria |
|---|---|---|---|
| 1 | [Discover](phases/01-discover.md) | Understand the workflow, not the feature request | Problem statement + success metric signed off |
| 2 | [Scope](phases/02-scope.md) | Smallest deployment that proves value | 1-page scope, risks, budget, approval rules |
| 3 | [Build & integrate](phases/03-build.md) | Working system on the client's real data and tools | Runs end-to-end on production data in a sandbox |
| 4 | [Deploy & harden](phases/04-deploy.md) | Live, observable, safe to fail | Monitoring, human-in-the-loop, rollback tested |
| 5 | [Hand off & learn](phases/05-handoff.md) | Client owns it; product team learns from it | Runbook delivered, metrics reviewed, feedback filed |

## Principles

1. **Start from the workflow, not the model.** Shadow the person who does the job today before writing code.
2. **One metric that the business already cares about.** Leads, hours saved, response time. Not "accuracy".
3. **Human approval before anything external.** Emails, posts, site changes and payments go through a review step until trust is earned.
4. **Cheap and boring infrastructure first.** A VPS, a database, cron and one model API beat a Kubernetes cluster for the first 10 clients.
5. **The model must never be a single point of failure.** Every AI step has a deterministic fallback.
6. **Leave it better documented than you found it.** Every deployment ships with a runbook.

## Templates

- [Discovery call checklist](templates/discovery-checklist.md)
- [One-page scope](templates/scope-one-pager.md)
- [Go-live checklist](templates/go-live-checklist.md)

## Reference deployments

| System | Stack | Pattern |
|---|---|---|
| AI SEO/GEO audit agent | Python, Claude API, WordPress | Audit → plan → approved fixes |
| Supplier outreach agent | Python, HubSpot, email, WhatsApp Business API | Assisted outreach with review queue |
| AI agency office | Self-hosted n8n, agent runtime, Telegram, VPS | AI "employees" with approval rules and daily reports |
| SEO workspace app | Google Cloud (Cloud SQL, Firebase Auth), GSC/GA4 OAuth | Multi-tenant SaaS on a single cloud project |

Open-source pieces: [`geo-audit-agent`](https://github.com/fde-nazmul/geo-audit-agent) · [`supplier-outreach-pipeline`](https://github.com/fde-nazmul/supplier-outreach-pipeline)

## License

MIT — reuse freely.
