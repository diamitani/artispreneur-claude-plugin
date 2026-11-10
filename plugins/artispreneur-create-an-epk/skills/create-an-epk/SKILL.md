---
name: create-an-epk
description: "EPK Builder: A press kit built for the person reading it — booker, press, brand, or festival. Use when an artist, manager or label asks for this (Studio)."
---

# EPK Builder

A press kit built for the person reading it — booker, press, brand, or festival.

Artispreneur desk: Press Team (desk plugin `artispreneur-press-team`, agent `artispreneur-press-team:press-team`). Category: Studio. Typical hands-on time: about 25 minutes.

## Ask the artist for

- Who the EPK is for (press, booking, brands, festivals, release campaign)
- Artist name, genre, city, and links
- Credits, shows, press, and numbers you can back up

## Deliverables

- Designed EPK web page + print-ready HTML (use Save as PDF), saved to My EPKs
- Audience-specific layout (booking, press, brand, general or one-sheet)
- Claim check: every stat sourced or removed

## Steps

1. Pick the audience variant and its section order
2. Collect facts, links, photos and sources
3. Run the claim validator; fix or drop unsourced claims
4. Build the designed EPK (web page + print-ready HTML, use Save as PDF)
5. Review readiness and fix what's missing in My EPKs

## Playbook

Goal: a finished, audience-specific EPK.
1. Ask which audience (general press, booking, partnerships, festival, release campaign). Call get_epk_variant_spec for it.
2. Collect: artist name, genre, location, links, focus track, credits, shows, press, stats — with a source for every material claim.
   Ask in ONE message for anything that makes the design premium and is missing: a press photo link (https), streaming/social links, releases (title, type, year, link, cover art link), real press quotes with outlet, past shows, rider notes. Never invent any of it.
3. Write the bio and highlights in the variant's order. Keep voice professional, active, no hype adjectives.
4. Call validate_epk with the draft. Resolve every missing item; source or remove every flagged claim.
5. Call build_complete_epk with every confirmed fact (and only those). Template: booking → "booking", press/release campaign → "media", partnerships → "brand", quick send → "one_sheeter", anything else → "general". This produces the designed web page + print-ready HTML (use Save as PDF) in My EPKs. Do NOT deliver the EPK with create_document; only use create_document if the artist explicitly asks for plain text.
6. Tell the artist the readiness stage and the top 3 things to add (from qa warnings / readiness.nextActions) so the next version looks even stronger, and point them to /app/epk.

## Guardrails

- Never fabricates press, stats, awards, or placements
- Unverified claims are dropped, not estimated
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`get_epk_variant_spec`, `validate_epk`, `build_complete_epk`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `create-an-epk` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Build my EPK. Ask me which audience it's for first, then gather my facts — only use numbers and credits I give you.
