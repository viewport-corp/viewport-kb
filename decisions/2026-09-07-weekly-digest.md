---
title: Viewport weekly anti-amnesia digest — 2026-09-07
date: 2026-09-07
period_start: 2026-08-31T09:00:55+07:00
period_end: 2026-09-07T09:18:36+07:00
source: scheduled-hermes
type: weekly-digest
status: reviewed
data_safety: public-safe-paraphrases-only
---

# 📊 VIEWPORT WEEKLY DIGEST — 2026-09-07

Coverage: after the prior digest cutoff on 2026-08-31 through 2026-09-07 09:18:36 Asia/Vientiane. The count uses canonical `chat-capture` issues and new KB idea/reference notes. Security follow-up #590 was already reported in the prior digest and is not double-counted.

CAPTURED THIS WEEK: **1 issue / 0 ideas / 2 references / 0 decisions / 0 corrections**

## GITHUB STATUS

Snapshot: **155 relevant issues open; 153 remain in the triage/review queue.** No relevant issue was closed during this coverage window, and only #590 and #591 changed.

### Open — captured this week

- [#591](https://github.com/viewport-corp/viewport-ops/issues/591) — Determine who introduced an unapproved external model-routing dependency, why it was configured, and whether it affected approved model use. This digest authorizes no provider activation or configuration change.

### Open — material carry-over

- [#590](https://github.com/viewport-corp/viewport-ops/issues/590) — Correct the intake pipeline so GitHub and KB receive semantic public-safe paraphrases, exact public reference links, safe summaries, and one canonical issue per inbound identity.
- [#578](https://github.com/viewport-corp/viewport-ops/issues/578) and [#588](https://github.com/viewport-corp/viewport-ops/issues/588) — The approved-model selection and usage-proof loop remains open with no new issue-side evidence during this window.
- `viewport-kb` pull requests [#1](https://github.com/viewport-corp/viewport-kb/pull/1), [#2](https://github.com/viewport-corp/viewport-kb/pull/2), and [#3](https://github.com/viewport-corp/viewport-kb/pull/3) remain open and unchanged; two contain older weekly digests that are still absent from `main`.

### Closed

- None during this coverage window.

### Blocked — persistent items

- [#192](https://github.com/viewport-corp/viewport-ops/issues/192) — Raw chat/session export remains blocked because the approved counts-only scan found credential-pattern hits. Keep the no-export boundary until redaction, rotation, and verification evidence exists.
- [#500](https://github.com/viewport-corp/viewport-ops/issues/500) and [#501](https://github.com/viewport-corp/viewport-ops/issues/501) — Duplicate Hermes/OpenClaw handoff tickets remain open. Consolidation still requires verified bidirectional delivery and runtime-admission evidence; an unverified mention is not proof.
- The two new reference notes cannot be fully analyzed from KB because only platform home-page URLs were preserved. Recovery is tracked under [#590](https://github.com/viewport-corp/viewport-ops/issues/590).

## KB GROWTH

- **2 new non-digest notes**, both reference captures:
  - [`references/2026-09-01-capture-and-analyze-shared-reference-link.md`](https://github.com/viewport-corp/viewport-kb/blob/main/references/2026-09-01-capture-and-analyze-shared-reference-link.md)
  - [`references/2026-09-05-capture-and-analyze-shared-reference-link.md`](https://github.com/viewport-corp/viewport-kb/blob/main/references/2026-09-05-capture-and-analyze-shared-reference-link.md)
- **References:** 2 added; **0 fully analyzed**. Both remain `captured-reference`; the stored summaries are uncurated site bootstrap output, not source-level analysis.
- **Ideas:** 0 added; **0 promoted**.
- **Decisions:** 0 non-digest decision notes added.
- Before publication, `INDEX.md` reported 65 notes. Publishing and indexing this digest raises the indexed count to **66**.
- `viewport-os/HANDOFF.md` still reports 2026-06-05 as its last update, so it is not reliable as a current handoff without GitHub issue evidence.

## REPEATED TOPICS ⚠️

- **Reference ingestion failed twice:** both new links were reduced to platform home pages and left as shallow captures. Consolidate remediation and acceptance tests under [#590](https://github.com/viewport-corp/viewport-ops/issues/590).
- **Capture-safety defects recur:** [#590](https://github.com/viewport-corp/viewport-ops/issues/590) overlaps older [#488](https://github.com/viewport-corp/viewport-ops/issues/488), while the newest issue and reference notes still show literal/truncated or uncurated capture behavior. Keep #590 as the proposed canonical security task; do not close or rewrite history without review.
- **Model/provider governance remains fragmented:** [#591](https://github.com/viewport-corp/viewport-ops/issues/591), [#578](https://github.com/viewport-corp/viewport-ops/issues/578), and [#588](https://github.com/viewport-corp/viewport-ops/issues/588) need one evidence packet covering attribution, approved provider boundaries, actual use, and remaining work.
- **Agent-handoff tracking is duplicated:** [#500](https://github.com/viewport-corp/viewport-ops/issues/500) and [#501](https://github.com/viewport-corp/viewport-ops/issues/501) still represent the same unresolved transport loop.

## NEEDS SAM REVIEW

- **Reference recovery:** if the two social-media references still matter, Sam must resend the exact public item links because the KB preserved only platform home pages. Hermes should then analyze the actual sources and update the same notes, not create duplicates.
- **Provider boundary:** no new approval is inferred. Hermes must answer [#591](https://github.com/viewport-corp/viewport-ops/issues/591) with attribution and current-state evidence first; Sam reviews only a later proposal to activate or change provider routing.
- **Protected remediation:** Sam approval is required only if [#590](https://github.com/viewport-corp/viewport-ops/issues/590) proposes rewriting Git history or deleting evidence. Sanitizer fixes, tests, and a counts-only inventory can proceed through normal GitHub review.
- **Stale KB pull requests:** Hermes should first review [#1](https://github.com/viewport-corp/viewport-kb/pull/1), [#2](https://github.com/viewport-corp/viewport-kb/pull/2), and [#3](https://github.com/viewport-corp/viewport-kb/pull/3) for safe merge versus supersession; escalate only if a policy or source-content decision remains.

## TOP 3 PRIORITIES — HERMES RECOMMENDATION

1. **Stop further bad captures under [#590](https://github.com/viewport-corp/viewport-ops/issues/590):** fix semantic paraphrasing, preserve exact public URLs, reject raw bootstrap payloads, enforce idempotency, and add adversarial tests before treating intake as healthy.
2. **Close the provider-attribution question under [#591](https://github.com/viewport-corp/viewport-ops/issues/591):** identify the introducing actor/commit/config path, explain purpose and actual use, compare against the approved provider boundary, and make no activation or routing change without a separate gate.
3. **Restore the control loop:** triage the 153-item review queue, consolidate #488/#590 and #500/#501, review the three stale KB pull requests, and refresh `viewport-os/HANDOFF.md` with current owners, blockers, and evidence instead of leaving capture as an unclosed backlog.

## Evidence and safety

Sources used: GitHub API for `viewport-corp/viewport-ops`; `viewport-corp/viewport-kb` `INDEX.md`, note tree, commits, reference metadata, and open pull requests; and `viewport-corp/viewport-os/HANDOFF.md`.

No raw Telegram/Hermes session export was read. No secret values are included. Existing unsafe-looking source fragments were not reproduced. No runtime, DNS, access, provider, or service state was changed.
