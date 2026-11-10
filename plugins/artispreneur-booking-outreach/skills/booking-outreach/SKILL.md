---
name: booking-outreach
description: "Booking Outreach: Venue and promoter outreach for the cities and dates you want. Use when an artist, manager or label asks for this (Outreach)."
---

# Booking Outreach

Venue and promoter outreach for the cities and dates you want.

Artispreneur desk: Outreach Team (desk plugin `artispreneur-outreach-team`, agent `artispreneur-outreach-team:outreach-team`). Category: Outreach. Typical hands-on time: about 20 minutes.

## Ask the artist for

- Target city/region and date range
- Draw you can honestly expect (or past show numbers)
- Your EPK link

## Deliverables

- Booking inquiry email template
- Matched venue/promoter list for your market
- Follow-up sequence
- Show tracker: venue, date, status, offer

## Steps

1. Set the market and dates
2. Write the inquiry
3. Match venues
4. Track to confirmed shows

## Playbook

Goal: booking inquiries that get answers, and a tracker to confirmed shows.
1. Ask city/region, date range, set length, honest expected draw (past numbers), and the EPK link. Suggest building or updating the EPK first if missing.
2. Inquiry email: who you are (one line), proposed dates, draw/history, what you're asking for (support slot, headline, residency), EPK link. Under 120 words.
3. Call search_directory for venues/promoters in the market (limit 15), matched by genre and capacity fit. Show for approval.
4. Follow-up at 7 days, final at 14 days.
5. Contacts: check manage_contacts so no venue is pitched twice; add each approved venue contact.
6. If Gmail is connected, queue each inquiry with run_app_action (contact_id set) for the artist's approval. Otherwise call create_document (type "pitch") with the inquiries and a show tracker (venue, contact, date requested, status, offer terms).

## Guardrails

- Never overstate draw — bookers check
- Never invent facts, numbers, contacts, or credits — ask, or leave it out.
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`, `search_directory`, `manage_contacts`, `find_app_actions`, `run_app_action`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `booking-outreach` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me book shows. I'll tell you the city and dates I want.
