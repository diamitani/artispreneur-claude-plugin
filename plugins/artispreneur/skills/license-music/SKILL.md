---
name: license-music
description: "Music Licensing Brief: Pitch-ready sync briefs and licensing basics, in plain English. Use when an artist, manager or label asks for this (Contracts)."
---

# Music Licensing Brief

Pitch-ready sync briefs and licensing basics, in plain English.

Artispreneur desk: Business Team (agent `artispreneur:business-team` in Claude Code). Category: Contracts. Typical hands-on time: about 15 minutes.

## Ask the artist for

- Tracks you want to license and who owns the master/publishing
- Mood, themes, and comparable artists
- Any existing licensing deals

## Deliverables

- Sync one-sheet per track (mood, tempo, themes, clearances)
- Licensing terms explained (master vs. sync, fees, territory)
- Pitch email template for music supervisors

## Steps

1. Confirm you control both sides (or who does)
2. Write track one-sheets
3. Explain terms you'll be offered
4. Write the pitch

## Playbook

Goal: sync-ready briefs.
1. Ask which tracks, who owns master and publishing, and splits. Flag anything not one-stop clearable.
2. For each track: title, duration, BPM (if known), mood tags, themes, instrumental availability, clearance status.
3. Explain master use vs. sync license, fee ranges depend on use/territory/term (don't quote fixed prices), MFN, and exclusivity.
4. Optionally search_directory for music supervisors/libraries; only name results returned.
5. Write a 120-word pitch email. Call create_document (type "pitch"). General information, not legal advice — review anything binding with a lawyer.

## Guardrails

- Flags any track you can't clear one-stop
- General information, not legal advice — review anything binding with a lawyer.
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`, `search_directory`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `license-music` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me get my music ready for sync licensing: track one-sheets, the terms I'll see, and a pitch email. Ask me about my catalog and who owns what first.
