---
name: artist-profile
description: "Artist Profile: One complete artist record (identity, genre, stage, city, links) with a career-stage assessment and gaps. Use when an artist, manager or label asks for this (Career)."
---

# Artist Profile

One complete artist record (identity, genre, stage, city, links) with a career-stage assessment and gaps.

Artispreneur desk: Home Base (agent `artispreneur:home-base` in Claude Code). Category: Career. Typical hands-on time: about 10 minutes.

## Ask the artist for

- Stage name (and legal name if different)
- Genres, city, and how long you've been releasing
- Your streaming and social links

## Deliverables

- Complete artist profile (identity, genre, stage, city, links)
- Career-stage assessment with reasons
- List of missing facts to add later

## Steps

1. Check what's already on file
2. Ask only for what's missing
3. Classify your career stage
4. Save the profile

## Playbook

Goal: one complete, accurate artist record that no other skill has to re-ask.
1. Review what the workspace already knows about the artist (profile, earlier conversations). List it back briefly.
2. Ask ONLY for missing fields, one short group at a time: stage name / legal name, genres (main + secondary), city and hometown, roles (singer, rapper, producer, songwriter, DJ, instrumentalist), year started, releases so far, live shows so far, streaming links, social links, booking email.
3. Classify career stage — new, developing, established, professional — from release count, show count and audience numbers the artist supplied. Explain the reason in one sentence.
4. Note gaps that weaken their materials (no press photo, no booking email, no latest release link).
5. Call create_document (type "doc") titled "Artist profile — <name>" with the record as a clean table, the stage assessment, and a short "add next" list.

## Guardrails

- Never invent facts, numbers, contacts, or credits — ask, or leave it out.
- Date of birth and phone stay private unless you say otherwise
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `artist-profile` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Set up my artist profile so every agent knows who I am. Ask only for what you don't already have.
