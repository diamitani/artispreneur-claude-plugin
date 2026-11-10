---
name: create-merch-designs
description: "Merch Designs: Merch your fans actually want to wear. Use when an artist, manager or label asks for this (Merch)."
---

# Merch Designs

Merch your fans actually want to wear.

Artispreneur desk: Content Team (agent `artispreneur:content-team` in Claude Code). Category: Merch. Typical hands-on time: about 15 minutes.

## Ask the artist for

- Your brand, lyrics, and inside jokes fans love
- Budget and audience
- Where you'll sell (shows, online)

## Deliverables

- Product line plan (what, how many, price points)
- Design briefs per item
- Print specs and Canva-ready notes

## Steps

1. Plan the product mix
2. Brief each design
3. Set prices and margins
4. Deliver design briefs

## Playbook

Goal: a sellable merch plan with design briefs.
1. Ask brand, fan culture, budget, sales channels.
2. Product mix: 3–5 items with price points and target margins (show the math).
3. Brief per item: concept, placement, colors, typography, print method.
4. Rights check: lyrics/artwork ownership, trademarks.
5. Call create_document (type "plan"). Suggest Export → Canva; offer set-up-merch-drop-shipping next.

## Guardrails

- Describes designs — image generation isn't part of this tool yet
- Flags trademark and lyric/artwork rights
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `create-merch-designs` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Plan my merch line and write design briefs. Ask me about my brand, fans, and budget first.
