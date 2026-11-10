---
name: create-llc
description: "LLC Formation: Separate your music money from your personal money. Use when an artist, manager or label asks for this (Legal entity)."
---

# LLC Formation

Separate your music money from your personal money.

Artispreneur desk: Business Team (desk plugin `artispreneur-business-team`, agent `artispreneur-business-team:business-team`). Category: Legal entity. Typical hands-on time: about 25 minutes.

## Ask the artist for

- State you live and operate in
- Solo or with partners
- Business name ideas

## Deliverables

- State-by-state filing plan for your state
- Operating agreement outline
- Post-filing checklist (EIN, bank, PRO publisher, DBA)

## Steps

1. Pick the formation state
2. Check name availability steps
3. Walk the state filing
4. Plan everything after approval

## Playbook

Goal: an LLC filing in motion.
1. Ask state, solo vs. partners, name ideas, and whether they already have an EIN or DBA.
2. Explain why most artists file in their home state; note any annual report/franchise obligations exist and must be checked on the state site.
3. Steps: name search on the Secretary of State site, registered agent, articles of organization, filing fee (tell them to confirm the current fee on the state site), operating agreement.
4. Outline an operating agreement (ownership, management, profit splits, what happens if a member leaves).
5. After approval: EIN (get-ein skill), business bank account, PRO publisher entity, bookkeeping.
6. Call create_document (type "checklist"). General information, not legal advice — review anything binding with a lawyer.

## Guardrails

- State fees vary — shown as a range to verify on your state's site
- General information, not legal advice — review anything binding with a lawyer.
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `create-llc` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Walk me through forming an LLC for my music business. Ask me which state I'm in and whether I have partners first.
