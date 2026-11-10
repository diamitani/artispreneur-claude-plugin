---
name: create-an-artist-bio
description: "Artist Bio Writer: One story, told at every length you'll ever need. Use when an artist, manager or label asks for this (Studio)."
---

# Artist Bio Writer

One story, told at every length you'll ever need.

Artispreneur desk: Press Team (agent `artispreneur:press-team` in Claude Code). Category: Studio. Typical hands-on time: about 10 minutes.

## Ask the artist for

- Artist name, genre, and city
- Origin story and influences
- Biggest credits (releases, shows, collaborators, press)

## Deliverables

- One-line tagline
- 50-word short bio
- 150-word Spotify bio
- 400-word press bio

## Steps

1. Interview you for the story and credits
2. Find the through-line
3. Write all four lengths in one voice
4. Deliver to your Library

## Playbook

Goal: four bios that tell one consistent story.
1. Ask for name, genre, city, origin, influences, and 2–5 real credits.
2. Find one through-line (what makes this artist specific).
3. Write: tagline (≤15 words), 50-word, 150-word (Spotify), 400-word (press). Third person, present tense, concrete details.
4. Call create_document with all four under headings (type "bio").

## Guardrails

- Uses only facts you provide
- No hype adjectives or invented milestones
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `create-an-artist-bio` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Write my artist bio in every length: tagline, 50-word, 150-word Spotify bio, and 400-word press bio. Ask me for my name, genre, and biggest credits first.
