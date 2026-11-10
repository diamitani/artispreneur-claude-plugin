---
name: royalty-readiness
description: "Royalty Readiness: Make sure every royalty stream you're owed has somewhere to land. Use when an artist, manager or label asks for this (Publishing & PRO)."
---

# Royalty Readiness

Make sure every royalty stream you're owed has somewhere to land.

Artispreneur desk: Business Team (desk plugin `artispreneur-business-team`, agent `artispreneur-business-team:business-team`). Category: Publishing & PRO. Typical hands-on time: about 15 minutes.

## Ask the artist for

- Are you registered with a PRO (ASCAP, BMI, SESAC)?
- SoundExchange, publishing admin, distributor status
- Upcoming or past releases

## Deliverables

- Royalty map: performance, mechanical, neighboring, master — who collects each
- Your registration status for each
- Ordered to-do list (what to register first)

## Steps

1. Explain the royalty types
2. Check each registration
3. Order the gaps
4. Hand off to registration tools

## Playbook

Goal: no royalties left uncollected.
1. Briefly explain the four streams in plain language: performance (PRO), mechanical (MLC in the US / publisher), digital performance for masters (SoundExchange), master royalties (distributor).
2. Ask status for each: PRO membership (writer and publisher), SoundExchange (artist and rights owner), MLC or publishing admin, distributor.
3. Map gaps to actions and order them by money at stake and release timing (release-blocking vs post-release).
4. Point to the matching skills: PRO Registration, Track Registration, Unclaimed Royalties.
5. Call create_document (type "checklist").

## Guardrails

- General information, not legal advice — review anything binding with a lawyer.
- Registration is done by the artist on official sites
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `royalty-readiness` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Am I set up to collect all my royalties? Check what I'm missing.
