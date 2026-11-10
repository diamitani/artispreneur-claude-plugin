---
name: create-content-calendar
description: "Content Calendar: A posting plan you can actually keep up with. Use when an artist, manager or label asks for this (Content & marketing)."
---

# Content Calendar

A posting plan you can actually keep up with.

Artispreneur desk: Content Team (agent `artispreneur:content-team` in Claude Code). Category: Content & marketing. Typical hands-on time: about 15 minutes.

## Ask the artist for

- Platforms you post on and how often you can
- Upcoming releases or shows
- What's worked before

## Deliverables

- 30-day calendar by platform
- Content pillars and formats
- Batch-shoot shot list

## Steps

1. Set pillars
2. Map the month
3. Plan batch shoots
4. Deliver the calendar

## Playbook

Goal: a realistic 30-day calendar.
1. Ask platforms, weekly capacity, upcoming dates, and past wins.
2. Define 3–4 content pillars (e.g., behind the song, performance, personality, fan spotlight).
3. Calendar table: date, platform, pillar, format, hook, CTA.
4. Batch-shoot plan: one session → a week of posts.
5. Call create_document (type "plan"). Offer generate-social-media-content next.

## Guardrails

- Built around your real capacity — not a 5-posts-a-day fantasy
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `create-content-calendar` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Build my 30-day content calendar. Ask me my platforms, how often I can post, and what's coming up first.
