---
name: media-outreach
description: "Media Pitching: Personal pitch emails for every journalist and blog on your list. Use when an artist, manager or label asks for this (Outreach)."
---

# Media Pitching

Personal pitch emails for every journalist and blog on your list.

Artispreneur desk: Outreach Team (agent `artispreneur:outreach-team` in Claude Code). Category: Outreach. Typical hands-on time: about 20 minutes.

## Ask the artist for

- Your PR hook or campaign (or run PR Campaign first)
- Your target list — or let the agent build one from the directory
- Your EPK link

## Deliverables

- One personalized draft per contact
- Tracking sheet: contact, outlet, stage, date sent, next follow-up
- Follow-up schedule

## Steps

1. Load the hook and list
2. Personalize each draft
3. Review together
4. Track and follow up

## Playbook

Goal: send-ready, personal pitches and a clean tracker.
1. Get the hook (from an earlier PR campaign or ask) and the EPK link.
2. Target list: use the artist's list, or call search_directory for outlets matching genre and outlet type (limit 15). Show the list for approval.
3. For each contact: one personalized opening line about the outlet (only what's public and verifiable, or ask), then the campaign's current-stage email.
4. Contacts: call manage_contacts (list) to skip anyone already pitched, then add each approved outlet contact.
5. If Gmail is connected (find_app_actions, app "gmail"), queue one send per contact with run_app_action, passing contact_id. Each email waits for the artist's approval; never say it was sent before they approve.
6. If Gmail isn't connected, call create_document (type "pitch") with all drafts and a tracker (contact, outlet, email, stage, sent date, next follow-up), and offer /app/connections.

## Guardrails

- Nothing sends without your approval: each email waits for your OK
- Never invent facts, numbers, contacts, or credits — ask, or leave it out.
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`, `search_directory`, `manage_contacts`, `find_app_actions`, `run_app_action`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `media-outreach` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Write personalized pitch emails for my press list. Use my PR hook and help me find outlets if I don't have a list.
