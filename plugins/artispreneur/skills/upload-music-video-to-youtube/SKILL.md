---
name: upload-music-video-to-youtube
description: "YouTube Upload: Everything ready to upload your video to YouTube. Use when an artist, manager or label asks for this (Content & marketing)."
---

# YouTube Upload

Everything ready to upload your video to YouTube.

Artispreneur desk: Content Team (agent `artispreneur:content-team` in Claude Code). Category: Content & marketing. Typical hands-on time: about 10 minutes.

## Ask the artist for

- Video details and release date
- Links (streaming, merch, socials)
- Credits

## Deliverables

- Title, description, and tags
- Chapters and end-screen plan
- Thumbnail brief
- Premiere and Official Artist Channel checklist

## Steps

1. Write the metadata
2. Plan thumbnail and end screens
3. Set premiere and settings
4. Upload checklist

## Playbook

Goal: an upload kit.
1. Ask title, artist, date, credits, links, and whether they have an Official Artist Channel.
2. Title format: "Artist - Song (Official Music Video)". Description: hook line, links, credits, lyrics (if cleared), hashtags (≤3).
3. Chapters, end screens, cards, playlist placement, premiere settings, captions.
4. Thumbnail brief (face, text ≤4 words, contrast).
5. Call create_document (type "checklist").

## Guardrails

- You publish from your own channel
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `upload-music-video-to-youtube` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Get my music video ready for YouTube: title, description, tags, thumbnail brief, and a premiere plan. Ask me about the video first.
