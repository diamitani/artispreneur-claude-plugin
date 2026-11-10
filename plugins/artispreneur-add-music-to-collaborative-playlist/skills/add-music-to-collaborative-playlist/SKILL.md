---
name: add-music-to-collaborative-playlist
description: "Playlist Pitching: Real playlist curators, honest pitches, no pay-for-play. Use when an artist, manager or label asks for this (Outreach)."
---

# Playlist Pitching

Real playlist curators, honest pitches, no pay-for-play.

Artispreneur desk: Booking Team (desk plugin `artispreneur-booking-team`, agent `artispreneur-booking-team:booking-team`). Category: Outreach. Typical hands-on time: about 15 minutes.

## Ask the artist for

- The track, genre, and mood
- Release date and links
- Comparable artists

## Deliverables

- Target list of curators from the live directory
- Pitch messages per curator type
- Follow-up and tracking sheet

## Steps

1. Search the directory for fitting curators
2. Qualify each target
3. Write the pitches
4. Track responses

## Playbook

Goal: a qualified curator list and pitches.
1. Ask genre, mood, comparables, release date, link.
2. search_directory for playlist curators in the genre; name only returned results.
3. Qualify: fit, activity, submission method. Warn against paid placements/bot playlists (DSP terms risk).
4. Short personalized pitch templates + follow-up cadence + tracking table.
5. Call create_document (type "target_list").

## Guardrails

- Only real curators from the directory
- Steers you away from pay-for-play and bot playlists
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`search_directory`, `create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `add-music-to-collaborative-playlist` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me pitch my song to playlists. Ask me the genre, mood, and release date, then search the directory for curators.
