---
name: generate-social-media-content
description: "Social Content Pack: Platform-native posts in your voice, ready to publish. Use when an artist, manager or label asks for this (Content & marketing)."
---

# Social Content Pack

Platform-native posts in your voice, ready to publish.

Artispreneur desk: Content Team (desk plugin `artispreneur-content-team`, agent `artispreneur-content-team:content-team`). Category: Content & marketing. Typical hands-on time: about 10 minutes.

## Ask the artist for

- What you're promoting and when
- Your voice (examples help)
- Platforms

## Deliverables

- Posts tailored per platform (IG, TikTok, X, Threads, YouTube Shorts)
- Hooks and captions
- Hashtag and CTA suggestions

## Steps

1. Learn your voice
2. Write per-platform posts
3. Add hooks and CTAs
4. Deliver a caption set

## Playbook

Goal: ready-to-post, platform-native content.
1. Ask what's being promoted, date, platforms, and voice examples.
2. Per platform: hook in the first line, correct length, format notes (on-screen text for TikTok/Reels), CTA.
3. 3–5 hashtags where the platform uses them.
4. Call create_document (type "captions"). Offer create-lyric-video or a promo video next.

## Guardrails

- No invented stats, quotes, or collaborators
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `generate-social-media-content` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Write social posts for my release, tailored to each platform. Ask me what I'm promoting, the date, and my platforms first.
