---
title: Viewport weekly anti-amnesia digest — 2026-08-03
date: 2026-08-03
source: scheduled-hermes
type: weekly-digest
status: captured
---

# Viewport weekly anti-amnesia digest — 2026-08-03

This digest uses public-safe paraphrases from GitHub and KB data only. It does not include raw Telegram or Hermes session content.

Reporting window: 2026-07-27 09:01 through 2026-08-03 09:00 Vientiane time.

## Captured this week

- Issues: 1
- Ideas: 0
- References: 1
- Decisions: 0
- Corrections: 0

Issue, decision, and correction counts use canonical GitHub labels. Reference and idea counts use new KB notes.

## GitHub status

### Open this week — 1

- #505 — Evaluate a loop-based workday/agent-workflow approach and convert the incomplete capture into a bounded task or durable architecture note.

### Closed this week — 0

- None among this week's captured issues.

### Backlog snapshot

- Relevant labeled issues: 130 open / 60 closed.
- Open issues still labeled `needs-triage`: 128.
- Formally blocked issues found by blocker/state labels: 0.

### Safety and quality gates

- #192 remains open: raw-history processing stays prohibited because the sensitive session store has credential-pattern hits. No session store was read for this digest.
- #488 remains open: permanent public-safe title sanitization and idempotency acceptance tests are not yet closed.
- #505 is not formally blocked, but the stored capture is incomplete; implementation should not be inferred from the truncated text.

## KB growth

- New notes: 2 including this digest.
- New reference notes: 1.
- New idea notes: 0.
- Ideas promoted from raw status: 0.
- References promoted to analyzed status: 0.
- `references/2026-08-02-capture-and-analyze-shared-reference-link.md` remains `captured-reference`; it resolves only to a generic TikTok landing-page capture and is not a completed source analysis.
- `INDEX.md` is updated by this change from 56 to 57 indexed notes.

## Repeated topics requiring consolidation

- No topic appeared twice among this week's two distinct captures.
- Cross-week reference debt persists: 11 KB notes use the generic `capture-and-analyze-shared-reference-link` slug. These should be mapped to exact sources, consolidated, promoted to analyzed references, or closed as unrecoverable.
- Weekly-digest publication is fragmented: five digest notes are indexed, while the 2026-07-27 digest remains in open PR #2. Review that PR before accumulating another unmerged digest.

## Needs Sam review

- #505 — confirm the exact loop-engineering source and desired deliverable; the public-safe capture is too incomplete for implementation.
- `references/2026-08-02-capture-and-analyze-shared-reference-link.md` — provide or recover the exact deep link if full analysis is still required.
- `viewport-kb` PR #2 — merge if the 2026-07-27 digest is accepted, or close/supersede it explicitly.
- #488 — assign the permanent sanitizer/idempotency fix; #505 shows that capture quality remains operationally weak.
- #192 — keep the raw-history security gate enforced until a separately approved remediation path exists.

## Top 3 priorities — Hermes recommendation

1. Repair intake quality under #488, then rewrite #505 into one public-safe, bounded loop-engineering task with acceptance criteria.
2. Recover and analyze the exact 2026-08-02 reference source; otherwise mark the shallow capture unrecoverable instead of leaving it as implied knowledge.
3. Resolve `viewport-kb` PR #2 and reduce the 128-item triage backlog, starting with security/active work; then refresh the stale `viewport-os/HANDOFF.md` through its own reviewed change.

## Proof and safety

Sources used: GitHub API for `viewport-corp/viewport-ops` labeled issues, `viewport-corp/viewport-kb` `INDEX.md`, note tree and commits, and `viewport-corp/viewport-os` `HANDOFF.md`.

No raw Telegram/Hermes session export was read. No matched credential values or secret values are included. No runtime, scheduler, route, access, or tenant data was changed.
