---
name: register-with-pro
description: "PRO Registration: Join ASCAP, BMI, or SESAC the right way — writer and publisher. Use when an artist, manager or label asks for this (Publishing & PRO)."
---

# PRO Registration

Join ASCAP, BMI, or SESAC the right way — writer and publisher.

Artispreneur desk: Release Team (desk plugin `artispreneur-release-team`, agent `artispreneur-release-team:release-team`). Category: Publishing & PRO. Typical hands-on time: about 20 minutes.

## Ask the artist for

- Country and whether you write/co-write your songs
- Any existing PRO, publisher, or admin deal
- Your legal name and any pen names

## Deliverables

- Which PRO fits you (and why)
- Writer registration walkthrough
- Self-publishing entity decision
- Checklist of what to have ready

## Steps

1. Choose a PRO
2. Register as a writer
3. Decide on a publisher entity
4. Plan work registrations next

## Playbook

Goal: the artist registered as a writer (and publisher if chosen).
1. Ask country, whether they write, existing PRO/publisher/admin deals, legal and pen names.
2. Compare ASCAP and BMI on what matters to them (both open to writers; SESAC is invitation-based). Tell them to confirm current fees/terms on each site.
3. Walk writer registration step by step; they submit on the PRO site.
4. Explain publisher shares and when a self-publishing entity or admin deal makes sense.
5. Next: register works (register-tracks-with-pro) and check The MLC/SoundExchange.
6. Call create_document (type "checklist").

## Guardrails

- One PRO per writer per territory — checks for conflicts first
- You submit on the PRO's site
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `register-with-pro` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me register with a PRO (ASCAP, BMI, or SESAC). Ask me where I'm based and whether I already have any deals first.
