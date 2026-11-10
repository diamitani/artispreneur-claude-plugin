---
name: set-up-dsp
description: "DSP Setup: Claim and polish your artist profiles on every streaming service. Use when an artist, manager or label asks for this (Release & DSP)."
---

# DSP Setup

Claim and polish your artist profiles on every streaming service.

Artispreneur desk: Release Team (desk plugin `artispreneur-release-team`, agent `artispreneur-release-team:release-team`). Category: Release & DSP. Typical hands-on time: about 15 minutes.

## Ask the artist for

- Your distributor
- Whether you have a release live
- Bio, photos, and links

## Deliverables

- Claim steps for Spotify, Apple Music, Amazon Music, YouTube (Official Artist Channel)
- Profile copy and image specs
- Pitching tools checklist

## Steps

1. Confirm a release is live
2. Claim each profile
3. Polish bio, images, and links
4. Set up pitching access

## Playbook

Goal: every artist profile claimed and polished.
1. Ask distributor, released music, bio, photos, socials.
2. Explain claiming usually requires a release delivered through a distributor.
3. Steps per platform: Spotify for Artists, Apple Music for Artists, Amazon Music for Artists, YouTube Official Artist Channel (usually via distributor).
4. Profile polish: bio (use create-an-artist-bio), image guidance, links, artist pick.
5. Checklist including editorial pitching access. Call create_document (type "checklist").

## Guardrails

- Claims need at least one release delivered by your distributor
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `set-up-dsp` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me set up my artist profiles on Spotify, Apple Music, Amazon, and YouTube. Ask me my distributor and whether I have music out first.
