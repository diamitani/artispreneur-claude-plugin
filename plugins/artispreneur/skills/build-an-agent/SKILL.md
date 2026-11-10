---
name: build-an-agent
description: "Build an Agent: Design a project sub-agent: mission, scope, skills, guardrails and starter prompts. Use when an artist, manager or label asks for this (Meta)."
---

# Build an Agent

Design a project sub-agent: mission, scope, skills, guardrails and starter prompts.

Artispreneur desk: Home Base (agent `artispreneur:home-base` in Claude Code). Category: Meta. Typical hands-on time: about 10 minutes.

## Ask the artist for

- The project (tour, album, brand deal, label)
- What success looks like
- Which tools it should lean on

## Deliverables

- Agent spec: mission, tools, guardrails
- A new team (sub-agent) in your workspace
- Starter prompts for the new agent

## Steps

1. Define the mission
2. Choose its tool set
3. Create the team
4. Hand off starter prompts

## Playbook

Goal: a working project sub-agent (team).
1. Ask the project, deadline, success criteria, and which areas it covers.
2. Pick the base team style that fits (main, business, press, release, booking, content) and the skills it should use.
3. Write a 1–2 sentence mission (it becomes the team tagline and guides the agent).
4. Call create_sub_agent with name, mission, base_kind.
5. Give 3 starter prompts for the new desk. Optionally create_document with the agent spec (type "plan").

## Guardrails

- Sub-agents only use tools your account has unlocked
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_sub_agent`, `create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `build-an-agent` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Build me a sub-agent for a specific project. Ask me what the project is and what success looks like first.
