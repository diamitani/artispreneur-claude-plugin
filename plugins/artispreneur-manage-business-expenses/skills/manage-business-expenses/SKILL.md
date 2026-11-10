---
name: manage-business-expenses
description: "Expense Manager: Know where every dollar goes — and keep the receipts that save you taxes. Use when an artist, manager or label asks for this (Finance)."
---

# Expense Manager

Know where every dollar goes — and keep the receipts that save you taxes.

Artispreneur desk: Business Team (desk plugin `artispreneur-business-team`, agent `artispreneur-business-team:business-team`). Category: Finance. Typical hands-on time: about 15 minutes.

## Ask the artist for

- What you spend on now (studio, gear, travel, promo, software)
- Current tools (app, spreadsheet, nothing)
- How you get paid

## Deliverables

- Expense categories built for musicians
- Tracking template (spreadsheet-ready)
- Weekly 15-minute money routine

## Steps

1. Build your category list
2. Set up the tracker
3. Create the weekly routine

## Playbook

Goal: a system the artist will actually use.
1. Ask current spending, tools, income streams.
2. Categories: studio/production, gear, software, marketing/ads, travel, merch COGS, contractors (collect W-9s), fees (distribution, PRO), home office, education.
3. Tracker: a table with date, vendor, category, amount, payment method, receipt link, business purpose.
4. Routine: weekly 15 minutes (log, snap receipts, reconcile), monthly review, quarterly tax set-aside check.
5. Call create_document (type "budget"). General information, not tax advice — confirm with a CPA or tax professional.

## Guardrails

- General information, not tax advice — confirm with a CPA or tax professional.
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `manage-business-expenses` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Set up expense tracking for my music business: categories, a tracker, and a simple weekly routine. Ask me what I spend on now first.
