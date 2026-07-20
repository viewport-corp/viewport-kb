---
title: Viewport weekly anti-amnesia digest — 2026-07-20
date: 2026-07-20
source: scheduled-hermes
type: weekly-digest
status: captured
---

# Viewport weekly anti-amnesia digest — 2026-07-20

This digest uses public-safe paraphrases from GitHub and KB data only. It does not include raw Telegram or Hermes session content.

## Captured this week

- Issues: 5
- Ideas: 0
- References: 0
- Decisions: 3
- Corrections: 0

## GitHub status

### Open this week

- #476 — Recover and verify OpenClaw within the approved fresh-runtime boundaries.
- #484 — Record approval for the scoped action under discussion.
- #485 — Resolve confusion between the fresh Dokploy/new-Docker path and legacy migration assumptions.
- #486 — Define the exact approval mechanism for protected actions.
- #487 — Establish evidence-based expectations for Hermes/OpenClaw reliability and current operational state.

### Closed this week

- None found among this week's captured issues.

### Blocked

- #192 — Raw chat-history processing remains blocked because a counts-only scan found credential-like patterns. No matched values are included here.

## KB growth

- `INDEX.md` was updated.
- `decisions/2026-07-13-weekly-digest.md` was added during the reporting window.
- `decisions/2026-07-20-weekly-digest.md` was created by this run.
- New reference notes: 0.
- New or promoted idea notes: 0.

## Repeated topics requiring consolidation

- **Approval workflow and operator authority:** #484 and #486 should point to one canonical approval protocol.
- **Hermes/OpenClaw recovery and reliability:** #476, #485, and #487 should be consolidated under one evidence-backed recovery/status thread.

## Needs Sam review

- #486 — Approve or amend the proposed canonical approval mechanism.
- #476 — Confirm the recovery task's exact protected-action gates and evidence needed for closure.
- #487 — Accept evidence-based reliability language rather than an absolute guarantee.
- #192 — Decide ownership and timing for safe remediation before any raw-history processing.

## Top 3 priorities — Hermes recommendation

1. Close #476 with live, redacted verification and link #485/#487 as context instead of running parallel recovery threads.
2. Consolidate #484/#486 into one durable approval protocol with exact examples for routine, protected, and production actions.
3. Keep #192 enforced and assign remediation; do not perform bulk chat-history processing until the security gate is cleared with evidence.

## Proof and safety

Sources used: GitHub API for `viewport-corp/viewport-ops` issues, `viewport-corp/viewport-kb` `INDEX.md`/note tree/commits, and `viewport-corp/viewport-os` `HANDOFF.md`.

No raw Telegram/Hermes session export was read. No secret values are included. No runtime change was made.
