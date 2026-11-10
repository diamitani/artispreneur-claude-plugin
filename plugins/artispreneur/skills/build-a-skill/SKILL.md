---
name: build-a-skill
description: "Build a Skill: Turn your workflow into a tool you can reuse, share, or sell. Use when an artist, manager or label asks for this (Meta)."
---

# Build a Skill

Turn your workflow into a tool you can reuse, share, or sell.

Artispreneur desk: Home Base (agent `artispreneur:home-base` in Claude Code). Category: Meta. Typical hands-on time: about 20 minutes.

## Ask the artist for

- The workflow you repeat (step by step)
- What a great result looks like
- Mistakes to avoid

## Deliverables

- A complete SKILL.md (name, description, playbook)
- Inputs, steps, and guardrails
- Packaging notes for Claude and other AI harnesses

## Steps

1. Interview you on the workflow
2. Structure it into a playbook
3. Add guardrails
4. Deliver a SKILL.md

## Playbook

Goal: a portable SKILL.md.
1. Ask the workflow step by step, inputs, output, quality bar, and failure modes.
2. Write a SKILL.md: YAML frontmatter (name: lowercase-hyphenated, description: when to use it in one sentence), then Goal, Ask first, Steps, Deliverable, Never.
3. Strip personal data/secrets.
4. Explain packaging: a folder with SKILL.md works in Claude Code (skills/<name>/SKILL.md) and similar harnesses.
5. Call create_document with the SKILL.md (type "doc").

## Guardrails

- Keeps your private data out of the published tool
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `build-a-skill` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me turn one of my workflows into a reusable AI tool. Ask me what the workflow is and what a great result looks like first.
