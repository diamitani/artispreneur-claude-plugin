---
name: brand-positioning
description: "Brand Positioning: The one true thing about you that no other artist in your genre can say. Use when an artist, manager or label asks for this (Studio)."
---

# Brand Positioning

The one true thing about you that no other artist in your genre can say.

Artispreneur desk: Content Team (desk plugin `artispreneur-content-team`, agent `artispreneur-content-team:content-team`). Category: Studio. Typical hands-on time: about 20 minutes.

## Ask the artist for

- Your genre and influences
- Your story — where you're from and what shaped you
- Who you make music for

## Deliverables

- One-paragraph positioning statement
- 3 tagline options
- Voice guide: 3 adjectives + 1 sentence on tone
- Story structure: origin → tension → proof → mission

## Steps

1. Find your authentic angle
2. Write the positioning statement
3. Draft taglines
4. Define your voice

## Playbook

Goal: positioning every other skill (EPK, bio, content, PR) can inherit.
1. Interview briefly: genre, influences, origin, a defining moment, who the music is for, what fans say about it.
2. Find the specific, true angle — something a generic artist in this genre could not say. Reflect it back and confirm.
3. Write a one-paragraph positioning statement: who, what sound, for whom, why now.
4. Write 3 tagline options (under 10 words each).
5. Voice: 3 adjectives + 1 sentence on tone; 3 "say this / not this" examples.
6. Story structure: origin → tension → proof → mission, one line each, using only stated facts.
7. Call create_document (type "doc") titled "Brand positioning — <name>".

## Guardrails

- Never invent facts, numbers, contacts, or credits — ask, or leave it out.
- No generic claims a thousand artists could make
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `brand-positioning` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me figure out my brand positioning — what makes me different. Ask me about my story first.
