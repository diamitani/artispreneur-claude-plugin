---
name: legal-business-checklist
description: "Business Setup Checklist: The business basics — entity, copyright, licensing, PRO — in the right order. Use when an artist, manager or label asks for this (Legal entity)."
---

# Business Setup Checklist

The business basics — entity, copyright, licensing, PRO — in the right order.

Artispreneur desk: Business Team (desk plugin `artispreneur-business-team`, agent `artispreneur-business-team:business-team`). Category: Legal entity. Typical hands-on time: about 15 minutes.

## Ask the artist for

- Which topic: business entity, copyright, licensing, or PRO
- What you've already done
- Your state (for entity questions)

## Deliverables

- Your business-readiness checklist with status
- Plain-language explanation of each item
- Real steps and typical fees, in order
- Which tool handles each next step

## Steps

1. Pick the topic
2. Explain it plainly
3. List the steps and fees
4. Hand off to the doing tool

## Playbook

Goal: the artist knows what's done, what's next and why.
1. Ask which topics matter now (entity/LLC, copyright, licensing, PRO) — don't cover all four unless asked — and what's already done.
2. For each topic: what it is and why it matters, in two sentences.
3. Steps in order with typical fees labelled as general and "check your state/official site": e.g. EIN (free from the IRS), LLC (state filing fee varies by state), copyright registration (US Copyright Office fee), PRO membership.
4. Status checklist: done / next / later.
5. Point each next step to the doing skill (EIN Registration, LLC Formation, PRO Registration, Split Sheet Agreement, Music Licensing Brief).
6. Call create_document (type "checklist").

## Guardrails

- General information, not legal advice — review anything binding with a lawyer.
- General information, not tax advice — confirm with a CPA or tax professional.
- Never collects SSNs or files anything for you
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `legal-business-checklist` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> What business and legal setup do I need as an artist? Walk me through it in order.
