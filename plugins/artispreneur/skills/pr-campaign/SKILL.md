---
name: pr-campaign
description: "PR Campaign: A 5-email press sequence built around one real, newsworthy hook. Use when an artist, manager or label asks for this (Outreach)."
---

# PR Campaign

A 5-email press sequence built around one real, newsworthy hook.

Artispreneur desk: Press Team (agent `artispreneur:press-team` in Claude Code). Category: Outreach. Typical hands-on time: about 25 minutes.

## Ask the artist for

- The release or milestone
- Target outlet types (blogs, magazines, podcasts, radio)
- Your EPK or links

## Deliverables

- The hook: what's newsworthy right now
- 5-stage email sequence: intro, follow-up, check-in, update, referral/close
- Dated campaign timeline (12 weeks)

## Steps

1. Confirm the hook
2. Write the intro email
3. Write the follow-ups
4. Date the campaign

## Playbook

Goal: a press campaign with a real hook and a sequence that respects editors' time.
1. Ask what's happening (release, milestone, story) and confirm what is genuinely newsworthy. Push back gently if the hook is weak and suggest a stronger angle from their facts.
2. Intro email (Week 1): genre, artist type, hometown, one verifiable highlight, sound in one line, why this outlet, link (EPK or track). Under 150 words, subject line options.
3. Follow-up (Week 2), check-in (Week 5), update with new news (Week 8), referral ask / polite close (Week 10–12). Each reuses the hook with a fresh reason to reply.
4. Dated timeline from the start date.
5. Offer to find matching outlets with search_directory (by genre and outlet type) — never guess contacts.
6. Call create_document (type "pitch") titled "PR campaign — <release>".

## Guardrails

- Never invent facts, numbers, contacts, or credits — ask, or leave it out.
- Drafts only — nothing is sent without your review
- No claims of press coverage you don't have
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`, `search_directory`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `pr-campaign` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Build me a press campaign for my release. Ask me what's newsworthy first.
