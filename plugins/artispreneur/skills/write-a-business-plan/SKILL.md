---
name: write-a-business-plan
description: "Business Plan: A real plan with real numbers — for you, a partner, or a lender. Use when an artist, manager or label asks for this (Finance)."
---

# Business Plan

A real plan with real numbers — for you, a partner, or a lender.

Artispreneur desk: Home Base (agent `artispreneur:home-base` in Claude Code). Category: Finance. Typical hands-on time: about 30 minutes.

## Ask the artist for

- Current income by source
- Monthly costs
- Goals for the next 12 months

## Deliverables

- One-page executive summary
- Revenue streams and 12-month projections
- Costs, budget, and break-even
- Milestones and KPIs

## Steps

1. Baseline where you are
2. Model revenue and costs
3. Set milestones
4. Write the plan

## Playbook

Goal: a credible, numbers-first business plan.
1. Ask current income by stream, monthly costs, audience size (only what they know), goals, and who the plan is for.
2. Sections: executive summary, artist/market positioning, revenue streams, 12-month projection table (state every assumption), cost budget, break-even, marketing plan, milestones with dates, KPIs.
3. Show the math. Label estimates as estimates.
4. Call create_document (type "plan"). Suggest Export → Google Slides for a pitch version.

## Guardrails

- Projections use your inputs with stated assumptions — nothing invented
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `write-a-business-plan` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Write my music business plan with real numbers. Ask me about my current income, costs, and goals first.
