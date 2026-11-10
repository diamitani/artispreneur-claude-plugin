---
name: get-ein
description: "EIN Registration: Your federal tax ID — free from the IRS, done step by step. Use when an artist, manager or label asks for this (Legal entity)."
---

# EIN Registration

Your federal tax ID — free from the IRS, done step by step.

Artispreneur desk: Business Team (desk plugin `artispreneur-business-team`, agent `artispreneur-business-team:business-team`). Category: Legal entity. Typical hands-on time: about 15 minutes.

## Ask the artist for

- Business structure (sole proprietor, LLC, corporation)
- Legal name and address
- Responsible party details — entered by you on IRS.gov only

## Deliverables

- Readiness checklist
- Question-by-question walkthrough of the IRS online application
- Where to store your EIN confirmation letter

## Steps

1. Confirm your structure
2. Prep every answer
3. Walk the IRS form one question at a time
4. You review and submit on IRS.gov

## Playbook

Goal: the artist gets an EIN on IRS.gov themselves.
1. Confirm structure (sole prop, single-member LLC, multi-member LLC, corporation). If no entity yet, mention LLC/C-corp skills first.
2. Prep answers: legal name, trade name (DBA), address, reason for applying, start date, employees expected.
3. Walk the IRS online EIN application one question at a time; confirm each answer before moving on.
4. Final review gate: list every answer for the artist to check. They submit on IRS.gov. The IRS charges no fee — warn about paid look-alike sites.
5. Never ask for, repeat, or store an SSN/ITIN; the artist types it directly into IRS.gov.
6. Call create_document with the checklist + their answers (no SSN) (type "checklist").

## Guardrails

- Never collects or stores your SSN
- You submit on IRS.gov yourself — the IRS charges nothing
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `get-ein` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Walk me through getting an EIN for my music business, one question at a time. Ask me about my business structure first.
