---
title: Viewport weekly anti-amnesia digest — 2026-07-27
date: 2026-07-27
source: scheduled-hermes
type: weekly-digest
status: captured
---

# Viewport weekly anti-amnesia digest — 2026-07-27

This digest uses public-safe paraphrases from GitHub and KB data only. It does not include raw Telegram or Hermes session content.

Reporting window: 2026-07-20 09:00 through 2026-07-27 09:01 Vientiane time.

## Captured this week

- Issues: 16
- Ideas: 0
- References: 2
- Decisions: 7
- Corrections: 1

Decision and correction counts use canonical GitHub labels. Reference and idea counts use new KB notes. Duplicate issue fanout is reported below rather than counted as additional underlying messages.

## GitHub status

### Open this week — 16

- #488 — Permanently sanitize Telegram-derived issue titles and digest output.
- #490 / #491 — Duplicate captures concerning legacy OpenClaw session-cleanup and retention risk.
- #492 / #493 — Duplicate captures requesting a complete central-brain/session-access follow-up.
- #494 / #495 — Duplicate captures correcting the response to a silent target agent.
- #496 — Validate the supported bot-to-bot communication path rather than relying on assumptions.
- #497 — Preserve complete inbound instructions for agent dispatch while persisting only public-safe summaries.
- #498 — Reconcile an activation/current-state claim with the actual prior state.
- #499 — Directed inter-agent handoff probe awaiting evidence-backed closure.
- #500 / #501 — Duplicate captures for the blocked private OpenClaw-to-Hermes handoff path.
- #502 — Convert the request for visible results into evidence-backed closure.
- #503 — Analyze the shared social-media reference rather than only capturing a generic landing page.
- #504 — Clarify an incomplete multi-agent/fallback decision capture before implementation.

### Closed this week — 0

- None among this week's captured issues.

### Blocked or risk-gated

- #192 remains open: bulk raw-history processing is prohibited because the sensitive session store has credential-like pattern hits. This digest did not read that store.
- #488 remains open: direct issue-title passthrough is prohibited until the sanitizer and acceptance test are fixed.
- #500 / #501 describe the same unproven private inter-agent delivery path; neither issue contains closure evidence.
- #504 is tagged as a blocker but its capture is truncated, so the exact decision is not safe to infer.

## KB growth

- New notes: 6 including this digest; five existed before this run.
- New reference notes: 2.
- New idea notes: 0.
- Ideas promoted from raw status: 0.
- References promoted to analyzed status: 0.
- `INDEX.md` is updated by this change.
- The two new reference notes remain shallow `captured-reference` entries based on generic Instagram/X landing pages; they are not completed source analyses.

## Repeated topics requiring consolidation

- **Duplicate canonicalization failure:** #490/#491, #492/#493, #494/#495, and #500/#501 are four same-message issue pairs. One inbound message should produce one canonical issue with multiple labels.
- **Inter-agent delivery and silence:** #494–#501 and #496 all concern delivery, acknowledgment, status, or bot-to-bot communication. Consolidate them under one evidence-backed handoff task with request IDs, receipts, timeouts, and bidirectional probes.
- **Central-brain and session continuity:** #490–#493 plus the two new decision notes repeat concerns about durable session access, cleanup, and Hermes/OpenClaw coordination. Convert them into one bounded retention and handoff policy.
- **Reference capture quality:** two generic social landing-page notes were created, but neither preserves enough source context for meaningful analysis. Consolidate or replace them only when the exact deep links are available.

## Needs Sam review

- #488 — Assign the permanent sanitizer/idempotency acceptance-test fix; the present digest is containment, not closure.
- #490 / #491 — Confirm the desired session-retention behavior before any cron, cleanup, archive, or runtime mutation.
- #500 / #501 — Keep one canonical private-handoff issue and require bidirectional live evidence before calling it available.
- #504 — Restate or repair the incomplete multi-agent/fallback decision capture before anyone implements it.
- #503 and the two new KB references — provide or recover the exact deep links if full source analysis is still required.

## Top 3 priorities — Hermes recommendation

1. Fix intake canonicalization and public-safe sanitization under #488, merge the four duplicate pairs, and add acceptance tests for one-message/one-issue behavior and no direct title passthrough.
2. Consolidate the Telegram/inter-agent issues into one handoff task and close it only with request ID, delivery receipt, acknowledgment, status, timeout, and bidirectional live-probe evidence.
3. Establish one session-retention and central-brain continuity policy from #490–#493, then update the stale `viewport-os/HANDOFF.md` only after read-only verification and any required protected-action approval.

## Proof and safety

Sources used: GitHub API for `viewport-corp/viewport-ops` issues, `viewport-corp/viewport-kb` `INDEX.md` and note tree, and `viewport-corp/viewport-os` `HANDOFF.md`.

No raw Telegram/Hermes session export was read. No matched credential values or secret values are included. No runtime, scheduler, route, access, or tenant data was changed.
