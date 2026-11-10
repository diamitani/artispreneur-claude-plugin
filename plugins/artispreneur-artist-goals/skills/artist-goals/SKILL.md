---
name: artist-goals
description: "Goal Setting: Turn \"I want to blow up\" into 1–3 dated goals you can actually hit. Use when an artist, manager or label asks for this (Career)."
---

# Goal Setting

Turn "I want to blow up" into 1–3 dated goals you can actually hit.

Artispreneur desk: Home Base (desk plugin `artispreneur-home-base`, agent `artispreneur-home-base:home-base`). Category: Career. Typical hands-on time: about 10 minutes.

## Ask the artist for

- What you want to happen (in your own words)
- Your timeframe
- Where you are today (numbers you know)

## Deliverables

- 1–3 measurable goals with a target number and a date
- Parked goals list
- The first concrete step toward the top goal

## Steps

1. Reflect the ambition in concrete terms
2. Pick 1–3 goals
3. Give each a number and a date
4. Name the first step

## Playbook

Goal: 1–3 goals that are definite, measurable and dated (One Must Act: name the 100 first).
1. Ask what they want in their own words, their timeframe, and where they are today (streams, list size, shows, income — only what they know).
2. Translate vague ambitions into concrete outcomes: "more fans" → mailing list size, monthly listeners, ticket sales; ask which matters most.
3. Keep at most 3 active goals; move the rest to a "parked" list with why.
4. For each goal: target number, date, how it will be measured, and the acceptable "close enough" result.
5. Name the single first step for the top goal, doable this week.
6. Call create_document (type "plan") titled "Goals — <name>".

## Guardrails

- Never invent facts, numbers, contacts, or credits — ask, or leave it out.
- Goals use the artist's own baseline numbers, never assumed ones
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `artist-goals` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me set real goals for my music career. I'll tell you what I want — turn it into something I can measure.
