---
name: distribution-readiness
description: "Distribution Readiness: Everything checked before you upload — and the right distributor for you. Use when an artist, manager or label asks for this (Release & DSP)."
---

# Distribution Readiness

Everything checked before you upload — and the right distributor for you.

Artispreneur desk: Release Team (agent `artispreneur:release-team` in Claude Code). Category: Release & DSP. Typical hands-on time: about 15 minutes.

## Ask the artist for

- Release type and date
- What's finished (masters, artwork, credits)
- Do you own all rights (samples, beats, features)?

## Deliverables

- Upload readiness checklist (masters, artwork, metadata, rights)
- Distributor comparison for your situation
- Blockers list with fixes

## Steps

1. Confirm rights
2. Check assets
3. Check metadata
4. Pick a distributor

## Playbook

Goal: no rejected uploads, no rights surprises.
1. Rights first: who owns the master and composition; any samples, leased beats or features need clearance/agreements. Flag anything unclear and suggest a split sheet or license review.
2. Assets: final masters (WAV, 44.1 kHz+ 16/24-bit), artwork (3000×3000 px, no URLs/logos of platforms, matches title), clean audio (no clipping).
3. Metadata: title, artist names/format, featured artists, writers and producers, ISRC (distributor can assign), UPC, genre, explicit flag, language, release date (allow 2–4 weeks lead).
4. Distributor comparison: pricing model (annual vs per-release vs commission), payout splits, YouTube Content ID, publishing admin — explain trade-offs for this artist; tell them to confirm current prices on each site.
5. Call create_document (type "checklist") with checklist, blockers and recommendation.

## Guardrails

- Unclear ownership (samples, leased beats) is flagged before upload
- General information, not legal advice — review anything binding with a lawyer.
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `distribution-readiness` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Am I ready to upload my release? Check everything and help me pick a distributor.
