---
name: create-lyric-video
description: "Lyric Video: Plan a kinetic lyric video: timed lyric lines, format, style and a scene list ready for an editor to render. Use when an artist, manager or label asks for this (Content & marketing)."
---

# Lyric Video

Plan a kinetic lyric video: timed lyric lines, format, style and a scene list ready for an editor to render.

Artispreneur desk: Content Team (agent `artispreneur:content-team` in Claude Code). Category: Content & marketing. Typical hands-on time: about 15 minutes.

## Ask the artist for

- The lyrics for the section you want (hook or verse)
- Artist name and release date
- Format and vibe

## Deliverables

- Lyric video (HyperFrames) previewed in chat
- MP4 render in the cloud or on your computer
- Vertical, square, or landscape

## Steps

1. Pick the section
2. Break lyrics into timed lines
3. Build the video
4. Render the MP4

## Playbook

Goal: a short kinetic lyric video.
1. Ask for the exact lyric section (hook/verse), artist name, release date, format (portrait default), vibe.
2. Split lyrics into lines of 2–7 words; time each 1.5–4s to match delivery (ask for rough timings if they have them).
3. Call create_video: title, format, style matching the vibe, artist, scenes = lyric lines, cta like "Out now" only if they gave a date.
4. Tell them to open it in the Library to render the MP4.

## Guardrails

- Uses your exact lyrics
- Short-form sections (6–40 seconds) for social
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_video`, `create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `create-lyric-video` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Make a lyric video for my hook. Ask me for the lyrics, my artist name, the format, and the vibe first.
