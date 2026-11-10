---
name: upload-track-to-catalogue
description: "Catalog Upload: One complete catalog record per track: metadata, credits, splits, rights and registration status. Use when an artist, manager or label asks for this (Catalogue)."
---

# Catalog Upload

One complete catalog record per track: metadata, credits, splits, rights and registration status.

Artispreneur desk: Release Team (agent `artispreneur:release-team` in Claude Code). Category: Catalogue. Typical hands-on time: about 10 minutes.

## Ask the artist for

- Track details and credits
- Release status
- Registration status (PRO, MLC, SoundExchange)

## Deliverables

- Catalog entry per track (metadata, credits, splits, status)
- Rights and registration status
- Next actions per track

## Steps

1. Collect track details
2. Record rights and splits
3. Log registration status
4. List next actions

## Playbook

Goal: a complete catalog record other skills can reuse.
1. Ask title, artists, credits, splits, ISRC/UPC, release status/date, and registrations.
2. Build the entry: metadata, rights (master owner, publishing), splits, registration status checklist.
3. List next actions (e.g., register with PRO, claim at The MLC).
4. Call create_document (type "doc").

## Guardrails

- Your catalog is private to your account
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `upload-track-to-catalogue` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Add a track to my catalog: metadata, credits, splits, and registration status. Ask me about the track first.
