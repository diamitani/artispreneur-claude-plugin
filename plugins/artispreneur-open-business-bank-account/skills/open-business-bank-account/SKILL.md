---
name: open-business-bank-account
description: "Business Bank Account: Walk into the bank (or app) with everything they'll ask for. Use when an artist, manager or label asks for this (Finance)."
---

# Business Bank Account

Walk into the bank (or app) with everything they'll ask for.

Artispreneur desk: Business Team (desk plugin `artispreneur-business-team`, agent `artispreneur-business-team:business-team`). Category: Finance. Typical hands-on time: about 10 minutes.

## Ask the artist for

- Entity type and state
- Monthly income and how you get paid (DSPs, shows, merch)
- Banking preferences

## Deliverables

- Document checklist for your entity type
- Questions to ask any bank
- Account setup plan (checking, savings for taxes, card)

## Steps

1. List required documents
2. Compare what matters (fees, deposits, integrations)
3. Plan your account structure

## Playbook

Goal: a bank-ready checklist and account plan.
1. Ask entity type, state, income sources, volume, and online vs. branch preference.
2. Document checklist by entity: ID, EIN letter (or SSN for sole props — they bring it, you never collect it), formation docs, operating agreement, DBA if used.
3. Comparison criteria: monthly fees, minimums, deposit methods (payouts from distributors/PayPal/Stripe), accounting integrations, FDIC insurance.
4. Suggest structure: operating checking + tax savings (set aside a % of income) + business card.
5. Call create_document (type "checklist").

## Guardrails

- No specific bank endorsements — criteria you can apply anywhere
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `open-business-bank-account` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Get me ready to open a business bank account for my music. Ask me my business type and how I get paid first.
