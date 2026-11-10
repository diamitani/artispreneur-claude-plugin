---
name: directory-search
description: "Industry Contact Finder: Plan a high-fit list of blogs, playlists, radio, podcasts, press and venues, and organize contacts you supply. Use when an artist, manager or label asks for this (Outreach)."
---

# Industry Contact Finder

Plan a high-fit list of blogs, playlists, radio, podcasts, press and venues, and organize contacts you supply.

Artispreneur desk: Booking Team (agent `artispreneur:booking-team` in Claude Code). Category: Outreach. Typical hands-on time: about 5 minutes.

## Ask the artist for

- Channel: blog, playlist, radio, podcast, press or venue
- Your genres
- Market/city (for venues)

## Deliverables

- Up to 15 matched contacts, ranked by fit
- Outreach-ready table (name, contact, channel, genres)
- Suggested next tool to pitch them

## Steps

1. Pick the channel
2. Match by genre and market
3. Rank by fit
4. Hand off to a pitch tool

## Playbook

Goal: a short, high-fit contact list ready for outreach.
1. Ask the channel (blog, playlist, radio, podcast, press, venue), genres, and market (venues).
2. Call search_directory filtered by channel + genre (+ market), limit 15.
3. Rank by genre match; drop poor fits. Never invent a contact or fill gaps from memory.
4. Present an outreach-ready table: name, outlet, contact method, channel, genres, notes.
5. Suggest the matching pitch skill (PR Campaign, Playlist Outreach, Booking Outreach) and offer to start it.
6. Call create_document (type "doc") with the list.

## Guardrails

- Results come only from the Artispreneur directory — never made up
- Returns a focused list, not the whole directory
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`search_directory`, `create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `directory-search` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Find me industry contacts that fit my music. Ask me which kind — blogs, playlists, radio, podcasts, press, or venues.
