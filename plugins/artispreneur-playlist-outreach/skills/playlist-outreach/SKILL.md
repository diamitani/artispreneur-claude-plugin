---
name: playlist-outreach
description: "Playlist Curator Pitching: Short, curator-friendly pitches matched to playlists in your genre. Use when an artist, manager or label asks for this (Outreach)."
---

# Playlist Curator Pitching

Short, curator-friendly pitches matched to playlists in your genre.

Artispreneur desk: Outreach Team (desk plugin `artispreneur-outreach-team`, agent `artispreneur-outreach-team:outreach-team`). Category: Outreach. Typical hands-on time: about 15 minutes.

## Ask the artist for

- Track link (or release date if pre-release)
- Genre and mood tags
- Comparable artists

## Deliverables

- Curator pitch template (link + 2 lines)
- Matched curator/playlist list from the directory
- Spotify editorial pitch draft (if pre-release)
- Tracking sheet

## Steps

1. Write the curator pitch
2. Match playlists by genre
3. Draft the editorial pitch
4. Track responses

## Playbook

Goal: pitches curators actually read, sent to playlists that fit.
1. Ask for the track link (or release date), genre/mood tags, comparable artists, and one standout fact.
2. Curator pitch: link + 1–2 lines (sound, mood, why it fits their list). Shorter than a press email.
3. If unreleased: draft the Spotify for Artists editorial pitch (submit at least 7 days before release; fields: genre, mood, instruments, story).
4. Call search_directory for playlist curators by genre (limit 15). Show matches for approval.
5. Warn clearly: never pay for placements.
6. Add approved curators to manage_contacts (role curator). If Gmail is connected and the curator takes email pitches, queue each with run_app_action (contact_id set) for approval; otherwise call create_document (type "pitch") with templates, matches and a tracker (curator, playlist, sent, response, added).

## Guardrails

- Never pay for placements — pay-for-play violates platform rules
- Never invent facts, numbers, contacts, or credits — ask, or leave it out.
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`, `search_directory`, `manage_contacts`, `find_app_actions`, `run_app_action`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `playlist-outreach` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me pitch my song to playlist curators. I'll give you the link and genre.
