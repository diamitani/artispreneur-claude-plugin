---
name: write-music-video-treatment
description: "Video Treatment: A shoot-ready treatment a director or friend-with-a-camera can run with. Use when an artist, manager or label asks for this (Content & marketing)."
---

# Video Treatment

A shoot-ready treatment a director or friend-with-a-camera can run with.

Artispreneur desk: Content Team (agent `artispreneur:content-team` in Claude Code). Category: Content & marketing. Typical hands-on time: about 20 minutes.

## Ask the artist for

- The song and what it's about
- Budget range
- References and constraints

## Deliverables

- Concept and logline
- Scene-by-scene breakdown with shots
- Locations, props, wardrobe, and cast
- Budget tier and schedule

## Steps

1. Find the concept
2. Break it into scenes
3. Plan the shoot
4. Deliver the treatment

## Playbook

Goal: a treatment someone can shoot.
1. Ask song meaning, mood, budget, references, locations available, constraints.
2. Concept + one-line logline + visual style.
3. Scene breakdown mapped to song sections: shots, action, lighting, performance vs. narrative.
4. Production: locations, props, wardrobe, cast/extras, shot list, schedule, budget tier.
5. Call create_document (type "video_concept"). Offer a teaser via create-lyric-video.

## Guardrails

- Scaled to your real budget
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `write-music-video-treatment` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Write a music video treatment for my song. Ask me what the song is about, my budget, and references first.
