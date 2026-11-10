---
name: weekly-win-plan
description: "Weekly Win Plan: Your top 3 moves this week, ranked by what actually moves the needle. Use when an artist, manager or label asks for this (Career)."
---

# Weekly Win Plan

Your top 3 moves this week, ranked by what actually moves the needle.

Artispreneur desk: Home Base (agent `artispreneur:home-base` in Claude Code). Category: Career. Typical hands-on time: about 5 minutes.

## Ask the artist for

- Your current goals (or set them first)
- Open projects and deadlines
- Hours you have this week

## Deliverables

- Top 1–3 actions for the week, ranked
- Who (which team) handles each
- What's overdue or blocked and how to unblock it

## Steps

1. Review goals and open work
2. Find what's overdue or blocked
3. Rank by impact vs effort
4. Hand off the top action

## Playbook

Goal: a short, ranked weekly plan that ends with action.
1. Pull the artist's goals and open projects from the workspace; if none exist, ask for their top goal and nearest deadline.
2. Ask how many hours they have this week.
3. Identify overdue items, blocked items (and what unblocks them), and the next step for each goal.
4. Rank candidates by impact on the top goal vs. effort and time; cap at 3.
5. For each action: what "done" looks like, the time it takes, and which team or skill runs it (e.g. Press team → Create an EPK).
6. Offer to start action #1 right now. Call create_document (type "plan") titled "Weekly win plan — <week>".

## Guardrails

- Never more than 3 actions — fewer, better actions
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `weekly-win-plan` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> What should I focus on this week? Look at my goals and open projects and give me my top 3 moves.
