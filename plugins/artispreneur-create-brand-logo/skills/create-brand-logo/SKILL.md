---
name: create-brand-logo
description: "Brand Logo: A logo brief a designer (or Canva) can execute on day one. Use when an artist, manager or label asks for this (Studio)."
---

# Brand Logo

A logo brief a designer (or Canva) can execute on day one.

Artispreneur desk: Business Team (desk plugin `artispreneur-business-team`, agent `artispreneur-business-team:business-team`). Category: Studio. Typical hands-on time: about 15 minutes.

## Ask the artist for

- Artist name and genre
- Visual references you love (and hate)
- Where the logo will live (streaming, merch, stage)

## Deliverables

- Brand positioning summary
- Three logo concepts described in detail
- Wordmark type and color recommendations
- Designer / Canva-ready brief

## Steps

1. Define the brand feel in three words
2. Develop three distinct concepts
3. Specify type, color, and lockups
4. Package a production brief

## Playbook

Goal: a logo brief ready for a designer or Canva.
1. Ask for name, genre, audience, references, and uses (avatar, merch, stage screen).
2. Name the brand feel in three words.
3. Write three distinct concepts: idea, wordmark style, icon (if any), and why it fits.
4. Specify typography (named typefaces), a 3–5 color palette with hex codes, and horizontal/stacked/avatar lockups.
5. Remind them to run a trademark search before finalizing.
6. Call create_document (type "doc"). Suggest Export → Canva.

## Guardrails

- Describes concepts — image generation isn't part of this tool yet
- Flags trademark checks before you commit
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `create-brand-logo` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me create my artist logo: three concepts, typography, colors, and a brief I can hand to a designer or build in Canva. Ask me about my sound and references first.
