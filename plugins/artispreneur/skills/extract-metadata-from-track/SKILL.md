---
name: extract-metadata-from-track
description: "Metadata Extractor: Clean, complete metadata for every track in your catalog. Use when an artist, manager or label asks for this (Catalogue)."
---

# Metadata Extractor

Clean, complete metadata for every track in your catalog.

Artispreneur desk: Release Team (agent `artispreneur:release-team` in Claude Code). Category: Catalogue. Typical hands-on time: about 10 minutes.

## Ask the artist for

- Track tags or a distributor export (paste them)
- Credits and splits
- Release details

## Deliverables

- Normalized metadata sheet (title, artists, credits, ISRC, UPC, genre, explicit)
- Missing-field report
- Distributor-ready formatting

## Steps

1. Collect raw metadata
2. Normalize and dedupe
3. Flag gaps
4. Deliver a clean sheet

## Playbook

Goal: complete, consistent metadata.
1. Ask the artist to paste file tags, a distributor export, or type the details. Be clear audio isn't analyzed in this version.
2. Normalize: title casing, featured artist format, credits (writers, producers, performers), ISRC, UPC, genre, explicit flag, release date, language.
3. Flag missing/conflicting fields and how to fix each.
4. Call create_document with a metadata table (type "doc").

## Guardrails

- Reads the tags and text you provide — audio analysis (BPM, key) is coming soon
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `extract-metadata-from-track` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Clean up my track metadata. I'll paste the tags or my distributor export — ask me what you need first.
