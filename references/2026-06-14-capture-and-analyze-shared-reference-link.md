---
title: Capture and analyze shared reference link
date: 2026-06-14T10:32:10.147735+00:00
source: telegram
type: link
url: https://core.telegram.org/bots/api#rich-message-formatting-options
status: analyzed-reference
tenant: viewport-internal
department: ops
tags: ["REFERENCE", "telegram", "bot-api", "rich-messages", "hermes-gateway", "companyos"]
updated: 2026-06-14T10:36:25.629861+00:00
---

# Capture and analyze shared reference link

## Source

- Reference: https://core.telegram.org/bots/api#rich-message-formatting-options
- Verified fetch: 2026-06-14 UTC
- Document hash observed by Hermes: `7169c59fab498cc6ddfd2d1d3f014b0f4a9e31cc7ca0d871874bf2dd213c0ee4`

## What changed in Telegram

Telegram Bot API 10.1 added **Rich Messages** for bots. This is bigger than normal `sendMessage` Markdown/HTML because bots can now send structured rich content through `sendRichMessage` and stream temporary generation previews through `sendRichMessageDraft`.

Officially supported rich-message capabilities include:

- headings `#` through `######`
- paragraphs, horizontal rules, block quotes, pull quotes/asides
- unordered, ordered, and task lists
- tables, including alignment and richer HTML table forms
- collapsible `<details>` blocks
- footnotes / references / in-document anchors
- formulas / LaTeX-style math blocks
- media blocks: photos, videos, audio, voice notes, animations
- collages and slideshows
- inline formatting: bold, italic, underline, strikethrough, spoiler, code, marked text, subscript, superscript, links, mentions, custom emoji, dates/times
- optional automatic entity detection bypass via `skip_entity_detection`

## Limits that matter

- Rich message text: up to **32768 UTF-8 characters**.
- Up to **500 blocks**.
- Up to **16 nested formatting/block levels**.
- Up to **50 media attachments**.
- Up to **20 table columns**.

## Why Sam shared this

This is directly relevant to Hermes / Viewport Telegram UX.

Current Hermes Telegram delivery already supports a limited markdown-to-Telegram conversion layer, but Telegram historically forced compromises around tables, long structured reports, rich media grouping, and streaming UX. Rich Messages create an official path for Telegram-native executive reports, evidence packets, launch QA reports, migration updates, task packets, and agent output that currently get flattened or split.

## Viewport relevance

High value for:

1. **Hermes Telegram final answers** — better tables, collapsible sections, proof blocks, footnotes, and media cards.
2. **Live AI streaming UX** — `sendRichMessageDraft` could replace awkward typing/progress patterns with ephemeral rich previews, then persist final output with `sendRichMessage`.
3. **Evidence reports** — structured checklists, tables, code blocks, screenshots/media groups, and collapsible logs can be sent cleanly to Sam.
4. **CompanyOS / task packets** — Telegram can become a better command surface for issues, approvals, status, and handoffs.
5. **Tenant bots** — client/associate bots can send polished rich reports without exposing internal dashboards.

## Adopt / do not adopt blindly

Verdict: **useful and should be tracked for Hermes Telegram gateway improvement**, but do not assume the current Hermes gateway already supports it.

Safe next path:

1. Check whether the installed Telegram bot library exposes `sendRichMessage` / `sendRichMessageDraft` yet.
2. Add a capability probe in Hermes Telegram platform startup.
3. Keep fallback to current markdown/HTML send path for unsupported libraries/clients.
4. Add a sanitizer/converter so model output cannot inject unsafe or invalid rich HTML.
5. Add tests for tables, details blocks, long reports, media blocks, and fallback behavior.
6. Pilot in a non-production bot/profile before enabling Sam's primary Hermes bot.

## Risks / caveats

- Telegram clients may render rich messages inconsistently while the feature is new.
- Existing bot SDKs may lag behind Bot API 10.1.
- Rich HTML allows much more structure, so Hermes needs a strict allowlist/sanitizer.
- `sendRichMessageDraft` previews are ephemeral and must be finalized by `sendRichMessage`.
- Media blocks require the bot to have permission to send the relevant media type.
- Paid broadcast fields exist in the same method surface; Hermes must not enable paid broadcast behavior by default.

## Recommended issue / task

Create a GitHub task for Hermes/Viewport:

**Title:** Add Telegram Bot API 10.1 Rich Messages capability probe and renderer fallback

Acceptance criteria:

- Detect whether `sendRichMessage` and `sendRichMessageDraft` are available for the configured Telegram adapter.
- Implement a safe renderer for executive reports and evidence packets.
- Preserve current markdown delivery fallback.
- Add tests and a sample rich report fixture.
- Verify in a non-production Telegram bot/profile first.
- Do not expose secrets, raw logs, or private customer data in rich messages.

## Status

Captured and analyzed. This should become a Hermes Telegram gateway enhancement candidate, not an immediate live-runtime mutation.
