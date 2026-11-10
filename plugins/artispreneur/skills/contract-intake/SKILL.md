---
name: contract-intake
description: "Contract Explainer: Understand any music contract in plain English before you sign. Use when an artist, manager or label asks for this (Contracts)."
---

# Contract Explainer

Understand any music contract in plain English before you sign.

Artispreneur desk: Business Team (agent `artispreneur:business-team` in Claude Code). Category: Contracts. Typical hands-on time: about 15 minutes.

## Ask the artist for

- The contract text (paste it) or a summary
- What kind of deal it is
- What matters most to you

## Deliverables

- Contract type and parties
- Plain-English summary of the key terms (term, rights, money, exclusivity, exit)
- Red-flag list vs. typical industry terms
- Questions to ask the other side

## Steps

1. Classify the deal
2. Explain each key term
3. Flag red flags
4. List questions for a lawyer

## Playbook

Goal: the artist understands what they're signing and what to ask.
1. Ask them to paste the contract (or describe it) and what they care about most.
2. Classify: management, booking, recording/label, producer, publishing, licensing/sync, split sheet, other.
3. Explain in plain English: parties, term length, territory, rights granted (and for how long), money (advances, royalty rates, commissions, recoupment), exclusivity, approvals, termination and exit, ownership after it ends.
4. Red flags vs. typical terms (e.g. perpetual rights, commission on income after the term, 360 clauses, unclear recoupment). Say what's typical in ranges, labelled as general.
5. Questions to ask and points to negotiate.
6. Close with: have an entertainment lawyer review before signing. Call create_document (type "doc").

## Guardrails

- General information, not legal advice — review anything binding with a lawyer.
- Always recommends a lawyer before signing
- Never signs or sends anything for you
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `contract-intake` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> I got a contract — help me understand it. I'll paste it in.
