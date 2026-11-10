---
name: claim-tracks-with-pro
description: "Unclaimed Royalties: Find and claim royalties already owed to you. Use when an artist, manager or label asks for this (Publishing & PRO)."
---

# Unclaimed Royalties

Find and claim royalties already owed to you.

Artispreneur desk: Release Team (agent `artispreneur:release-team` in Claude Code). Category: Publishing & PRO. Typical hands-on time: about 20 minutes.

## Ask the artist for

- Your catalog (titles, writers, ISRCs)
- Your PRO and registrations
- Any statements showing gaps

## Deliverables

- Search plan across PRO, The MLC, and SoundExchange
- Claim checklist per missing work
- Dispute/correction message templates

## Steps

1. Search each database
2. Match missing or wrong entries
3. File claims and corrections
4. Track outcomes

## Playbook

Goal: unclaimed money found and claimed.
1. Ask for catalog details and current registrations (PRO, The MLC, SoundExchange, publisher/admin).
2. Search plan: PRO repertoire search, The MLC portal (US mechanicals), SoundExchange (digital performance of recordings), YouTube Content ID.
3. For each gap: what's missing, where to claim, what documentation to have (split sheets, ISRCs).
4. Correction/dispute email templates. Tracker for claim status.
5. Only claim works they own or co-own. Call create_document (type "checklist").

## Guardrails

- Only claims what you actually own or co-own
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `claim-tracks-with-pro` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me find and claim royalties I'm owed. Ask me for my catalog and which organizations I'm registered with first.
