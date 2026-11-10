---
name: create-split-sheet-agreement
description: "Split Sheet Agreement: Everyone's share, in writing, before the song blows up. Use when an artist, manager or label asks for this (Contracts)."
---

# Split Sheet Agreement

Everyone's share, in writing, before the song blows up.

Artispreneur desk: Business Team (desk plugin `artispreneur-business-team`, agent `artispreneur-business-team:business-team`). Category: Contracts. Typical hands-on time: about 10 minutes.

## Ask the artist for

- Song title and date
- Every contributor, their role, and agreed percentage
- PRO and publisher info (if known)

## Deliverables

- Split sheet with writers, roles, and percentages
- PRO/IPI and publisher fields
- Signature and date block
- How-to-bring-it-up talking points

## Steps

1. Collect contributors and roles
2. Check splits total exactly 100%
3. Fill PRO/publisher fields
4. Deliver a signable draft

## Playbook

Goal: a signable split sheet.
1. Ask for song title, date, each writer/producer, role, agreed %, PRO, IPI, and publisher.
2. Verify the writer shares total exactly 100% (and master/producer points separately if relevant). If not, stop and resolve.
3. Build the sheet: song info, table of contributors, publisher/PRO fields, signature + date lines for everyone.
4. Add 3 talking points for raising splits early and a note: General information, not legal advice — review anything binding with a lawyer.
5. Call create_document (type "contract").

## Guardrails

- Won't finalize unless splits total 100%
- General information, not legal advice — review anything binding with a lawyer.
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `create-split-sheet-agreement` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Draft a split sheet for my song. Ask me the title, every collaborator, their role, and the agreed percentages first.
