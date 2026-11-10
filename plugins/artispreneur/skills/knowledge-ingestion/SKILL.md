---
name: knowledge-ingestion
description: "Teach Your Agent: Turn pasted bios, contracts and past EPKs into confirmed, structured facts and a list of conflicts. Use when an artist, manager or label asks for this (Meta)."
---

# Teach Your Agent

Turn pasted bios, contracts and past EPKs into confirmed, structured facts and a list of conflicts.

Artispreneur desk: Home Base (agent `artispreneur:home-base` in Claude Code). Category: Meta. Typical hands-on time: about 10 minutes.

## Ask the artist for

- The document (paste the text)
- What it should be used for (EPK, contract, brand, finances)

## Deliverables

- Facts extracted from your document, for your artist record
- Summary routed to the right team
- List of conflicts with what's already on file

## Steps

1. Classify the document
2. Extract the facts
3. Check for conflicts
4. Confirm and save

## Playbook

Goal: the artist's existing documents become reusable, confirmed facts.
1. Ask them to paste the document and say what it's for.
2. Classify the domain (bio/EPK, contract, brand, release, finance).
3. Extract structured facts: names, credits, releases, dates, links, press quotes (exact words + outlet), terms. Skip and warn about any sensitive personal data.
4. Compare with what's already on file and list conflicts for the artist to resolve.
5. Show the extracted facts for confirmation; only confirmed facts count.
6. Call create_document (type "note") titled "Knowledge — <document>", and suggest the skill that should use it next.

## Guardrails

- You confirm every fact before it's saved
- Sensitive data (SSNs, bank numbers) is never stored
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `knowledge-ingestion` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> I want to teach you about me. I'll paste a bio, old EPK, or contract — pull out the facts.
