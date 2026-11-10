---
name: write-brand-guidelines
description: "Brand Guidelines: Your brand bible: voice, visuals, and rules everyone follows. Use when an artist, manager or label asks for this (Studio)."
---

# Brand Guidelines

Your brand bible: voice, visuals, and rules everyone follows.

Artispreneur desk: Business Team (desk plugin `artispreneur-business-team`, agent `artispreneur-business-team:business-team`). Category: Studio. Typical hands-on time: about 20 minutes.

## Ask the artist for

- Existing logo, colors, and fonts (if any)
- Three words you want fans to feel
- Examples of posts or visuals you're proud of

## Deliverables

- Brand story and positioning
- Voice & tone rules with examples
- Palette, type, and logo usage
- Social, merch, and press rules

## Steps

1. Capture your identity
2. Codify voice with do/don't examples
3. Lock visual rules
4. Deliver a shareable brand guide

## Playbook

Goal: a brand guide collaborators can follow without asking.
1. Ask for current logo/colors/fonts, audience, three feeling words, and good/bad examples.
2. Write: brand story (100 words), positioning line, voice rules (5 do's, 5 don'ts with example sentences).
3. Visual rules: palette with hex + usage ratio, type hierarchy, logo clear space and misuse.
4. Channel rules: social, merch, press photos, collaborator checklist.
5. Call create_document (type "doc"). Suggest Export → Google Slides or PowerPoint for sharing.

## Guardrails

- Builds on what you already have — no forced rebrand
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `write-brand-guidelines` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Write my artist brand guidelines: voice, palette, type, logo usage, and social rules. Ask me about my current visuals and vibe first.
