---
name: analyze-social-media-engagement
description: "Engagement Audit: See what's working, what's not, and what to post next. Use when an artist, manager or label asks for this (Content & marketing)."
---

# Engagement Audit

See what's working, what's not, and what to post next.

Artispreneur desk: Content Team (desk plugin `artispreneur-content-team`, agent `artispreneur-content-team:content-team`). Category: Content & marketing. Typical hands-on time: about 15 minutes.

## Ask the artist for

- Your insights numbers (paste them) for recent posts
- Goals (followers, streams, ticket sales)
- Posting frequency

## Deliverables

- Engagement audit by platform and format
- Top and bottom posts with reasons
- Five concrete changes for next month

## Steps

1. Collect your numbers
2. Compare formats and topics
3. Find patterns
4. Recommend changes

## Playbook

Goal: an honest audit with next steps.
1. Ask platforms, goals, and to paste recent post stats (reach, likes, comments, shares, saves, follows).
2. Compute engagement rate per post; group by format, topic, time.
3. Top 3 / bottom 3 with likely reasons. Clearly separate their data from general guidance.
4. Five specific changes for next month and what metric to watch.
5. Call create_document (type "doc").

## Guardrails

- Only analyzes numbers you provide — never invents benchmarks as your data
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `analyze-social-media-engagement` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Audit my social media engagement. I'll paste my recent post numbers — ask me which platforms and goals first.
