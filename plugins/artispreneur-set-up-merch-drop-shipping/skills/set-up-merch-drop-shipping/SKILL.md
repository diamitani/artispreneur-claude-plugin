---
name: set-up-merch-drop-shipping
description: "Merch Fulfillment: Print-on-demand merch with zero inventory risk. Use when an artist, manager or label asks for this (Merch)."
---

# Merch Fulfillment

Print-on-demand merch with zero inventory risk.

Artispreneur desk: Business Team (desk plugin `artispreneur-business-team`, agent `artispreneur-business-team:business-team`). Category: Merch. Typical hands-on time: about 20 minutes.

## Ask the artist for

- Your designs (or design briefs)
- Where you want to sell (your site, Shopify, Bandcamp)
- Target price points

## Deliverables

- Print-on-demand platform comparison criteria
- Store setup steps
- Pricing and margin calculator
- Launch checklist

## Steps

1. Choose a POD approach
2. Connect it to your store
3. Price for margin
4. Launch the drop

## Playbook

Goal: a POD store ready to launch.
1. Ask storefront, designs, price targets, regions.
2. Compare POD options on criteria (product catalog, print quality, base cost, shipping regions, store integrations) — tell them to verify current pricing.
3. Setup steps: create account, upload designs/mockups, connect storefront, shipping and tax settings, test order.
4. Margin table: base cost, shipping, platform fees, retail, profit.
5. Launch checklist + announcement posts. Call create_document (type "checklist").

## Guardrails

- Shows margin math before you set prices
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `set-up-merch-drop-shipping` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Set up print-on-demand merch for me. Ask me where I want to sell and my target prices first.
