---
name: register-tracks-with-pro
description: "Track Registration: Register every song so royalties can actually find you. Use when an artist, manager or label asks for this (Publishing & PRO)."
---

# Track Registration

Register every song so royalties can actually find you.

Artispreneur desk: Release Team (desk plugin `artispreneur-release-team`, agent `artispreneur-release-team:release-team`). Category: Publishing & PRO. Typical hands-on time: about 15 minutes.

## Ask the artist for

- Song titles, writers, and splits
- Each writer's PRO and IPI (if known)
- Release info (ISRC, release date)

## Deliverables

- Work registration sheet per song
- Split and IPI verification
- Registration walkthrough for your PRO

## Steps

1. Collect song data
2. Verify splits total 100%
3. Walk the registration
4. Track confirmations

## Playbook

Goal: every song registered correctly.
1. Ask for each work: title, alternate titles, writers + roles + splits, each writer's PRO/IPI, publisher, ISRC/release date.
2. Verify writer splits total 100% per song; resolve before continuing (point to create-split-sheet-agreement if undocumented).
3. Walk the PRO's work registration form step by step; they submit.
4. Build a registration tracker (song, date submitted, work ID, status).
5. Call create_document (type "checklist").

## Guardrails

- Won't register splits that don't total 100%
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `register-tracks-with-pro` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me register my songs with my PRO. Ask me for each song's title, writers, and splits first.
