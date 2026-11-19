# Phase 4 — Deploy & harden

**Goal:** live, observable and safe to fail.

## Do
- Deploy to boring infrastructure the client can afford to keep running (VPS or a single cloud project).
- Back up before touching any client system (site, CRM, database).
- Turn on the human-in-the-loop path first; widen autonomy only after a clean track record.
- Add monitoring: job success/failure, cost per day, volume, and the success metric.
- Send a daily or weekly summary to where the client already reads (email, Telegram, Lark).
- Test rollback for real at least once.

## Output
Go-live checklist completed (see [template](../templates/go-live-checklist.md)).
