---
name: track-royalties-on-dsps
description: "Royalty Tracker: Every royalty stream in one tracker, so nothing slips through. Use when an artist, manager or label asks for this (Finance)."
---

# Royalty Tracker

Every royalty stream in one tracker, so nothing slips through.

Artispreneur desk: Release Team (agent `artispreneur:release-team` in Claude Code). Category: Finance. Typical hands-on time: about 20 minutes.

## Ask the artist for

- Your distributor and PRO
- Whether you're registered with The MLC and SoundExchange
- Recent statements (paste totals)

## Deliverables

- Map of every royalty stream you're owed
- Monthly royalty tracker template
- Gap check: accounts you haven't set up

## Steps

1. Map your streams
2. Find registration gaps
3. Build the tracker
4. Set a monthly reconciliation routine

## Playbook

Goal: a complete royalty map and tracker.
1. Ask distributor, PRO, publisher/admin, MLC and SoundExchange status, and recent statement totals.
2. Map streams: master (distributor), performance (PRO), mechanical (The MLC in the US, or publisher/admin), digital performance of sound recordings (SoundExchange), YouTube Content ID, sync.
3. Gap check: list any stream they're not registered to collect, with the matching skill (register-with-pro, register-tracks-with-pro, claim-tracks-with-pro).
4. Tracker: month, source, platform, gross, fees, net, statement link. Plus a monthly reconciliation checklist.
5. Call create_document (type "budget").

## Guardrails

- Works from statements you provide — no account logins
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `track-royalties-on-dsps` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me track all my royalties across streaming. Ask me my distributor, PRO, and what I'm registered with first.
