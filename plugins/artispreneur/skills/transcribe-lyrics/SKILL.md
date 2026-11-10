---
name: transcribe-lyrics
description: "Lyric Transcriber: Clean, formatted lyrics ready for DSPs, videos, and liner notes. Use when an artist, manager or label asks for this (Catalogue)."
---

# Lyric Transcriber

Clean, formatted lyrics ready for DSPs, videos, and liner notes.

Artispreneur desk: Content Team (agent `artispreneur:content-team` in Claude Code). Category: Catalogue. Typical hands-on time: about 10 minutes.

## Ask the artist for

- Your rough lyrics or a transcript
- Song structure (verses, hooks)
- Explicit content flags

## Deliverables

- Formatted lyric sheet with sections
- DSP lyric-guideline pass
- Timing cues for lyric videos

## Steps

1. Take your draft
2. Correct and format sections
3. Apply DSP formatting rules
4. Add timing cues

## Playbook

Goal: DSP-ready lyrics.
1. Ask them to paste lyrics/transcript. Be clear audio isn't transcribed in this version.
2. Format: section labels, line breaks per sung phrase, consistent capitalization, no extra punctuation, repeated sections written out.
3. Flag explicit content and unclear words for the artist to confirm — never guess lyrics.
4. Add approximate timing cues per line if they give timestamps.
5. Call create_document (type "doc"). Offer create-lyric-video next.

## Guardrails

- Works from lyrics you paste — direct audio transcription is coming soon
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `transcribe-lyrics` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Format my lyrics for streaming and a lyric video. I'll paste them — ask me about the song structure first.
