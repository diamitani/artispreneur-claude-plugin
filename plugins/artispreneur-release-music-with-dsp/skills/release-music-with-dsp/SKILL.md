---
name: release-music-with-dsp
description: "Release Engine: A release plan that works backward from drop day. Use when an artist, manager or label asks for this (Release & DSP)."
---

# Release Engine

A release plan that works backward from drop day.

Artispreneur desk: Release Team (desk plugin `artispreneur-release-team`, agent `artispreneur-release-team:release-team`). Category: Release & DSP. Typical hands-on time: about 25 minutes.

## Ask the artist for

- Release title, type, and date
- Distributor
- Budget and promo assets you have

## Deliverables

- Dated rollout timeline counted back from release
- Distribution and metadata checklist (ISRC, UPC, credits)
- Editorial pitch plan
- Drop-week daily checklist

## Steps

1. Set the timeline from release date
2. Prep metadata and upload
3. Pitch editorial in time
4. Run drop week

## Playbook

Goal: a dated rollout that ships on time.
1. Ask title, single/EP/album, release date, distributor, budget, assets.
2. Timeline counted back: final masters + artwork, distributor upload (allow 2–4 weeks), pre-save, Spotify editorial pitch at least 7 days before release, content schedule, press/playlist outreach.
3. Metadata checklist: credits, ISRCs, UPC, explicit flag, lyrics, splits documented.
4. Drop-week checklist by day. Post-release: first 30 days.
5. Call create_document (type "rollout").

## Guardrails

- Builds in distributor lead time and the 7-day editorial pitch window
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `release-music-with-dsp` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Build my release plan working back from my release date. Ask me the title, date, distributor, and budget first.
