---
name: budget-planning
description: "Budget & Runway: A plain-language budget and runway for your release, tour, or year. Use when an artist, manager or label asks for this (Finance)."
---

# Budget & Runway

A plain-language budget and runway for your release, tour, or year.

Artispreneur desk: Business Team (desk plugin `artispreneur-business-team`, agent `artispreneur-business-team:business-team`). Category: Finance. Typical hands-on time: about 15 minutes.

## Ask the artist for

- The project or period
- Money in (income) and money out (expenses) — rough is fine
- The decision you're facing

## Deliverables

- Budget by category (recording, marketing, travel, gear, fees)
- Runway: months of funds at your current spend
- Answer to your spend question ("can I afford X?")
- One recommended money move

## Steps

1. Gather the numbers
2. Categorize
3. Calculate runway
4. Answer the question

## Playbook

Goal: a budget a non-accountant can use to decide.
1. Ask the project/period, available funds, expected income, and known or planned expenses. Rough numbers are fine; label estimates.
2. Categorize: recording/mixing/mastering, artwork/video, marketing/ads, PR, distribution fees, travel, gear, other.
3. Compute totals, the gap, and runway = available funds ÷ average monthly spend.
4. Answer the specific question ("can I afford a $2,000 video?") with the trade-off.
5. Recommend one money move (cut, delay, fund, or proceed). Defer tax questions to a professional.
6. Call create_document (type "budget") with a table.

## Guardrails

- General information, not tax advice — confirm with a CPA or tax professional.
- Uses only the numbers you give — no guessing your finances
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `budget-planning` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me budget for my release (or tour). I'll give you rough numbers.
