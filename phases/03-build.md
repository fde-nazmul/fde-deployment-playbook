# Phase 3 — Build & integrate

**Goal:** a working system on the client's real data and real tools, end-to-end, as early as possible.

## Do
- Build the thinnest end-to-end slice first (input → AI step → review → output), then deepen.
- Integrate with the tools the client already uses (WordPress, HubSpot, Search Console, Telegram) rather than adding new UIs.
- Keep prompts, rules and thresholds in config, not code, so they can be tuned without a deploy.
- Write an evaluation set from the samples collected in Discover and run it on every change.
- Wrap every model call with: timeout, retry, budget check, fallback, and a log line.

## Output
System runs end-to-end on production data in a sandbox; evaluation results shared with the client.
