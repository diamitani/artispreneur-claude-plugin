---
name: create-c-corp
description: "C-Corp Formation: Incorporate for investors, a label, or scale — with eyes open. Use when an artist, manager or label asks for this (Legal entity)."
---

# C-Corp Formation

Incorporate for investors, a label, or scale — with eyes open.

Artispreneur desk: Business Team (desk plugin `artispreneur-business-team`, agent `artispreneur-business-team:business-team`). Category: Legal entity. Typical hands-on time: about 30 minutes.

## Ask the artist for

- Revenue today and goals
- Plans to raise money or bring in partners
- State of operation

## Deliverables

- Is a C-corp right for you? decision memo
- Incorporation steps (state, articles, bylaws, board, shares)
- Post-incorporation compliance checklist

## Steps

1. Test whether an LLC or S-corp election fits better
2. Choose the state
3. Walk incorporation filings
4. Set up compliance

## Playbook

Goal: a clear decision, then a filing plan.
1. Ask revenue, goals (investors, label, employees), partners, state.
2. Decision memo: C-corp pros (investment-ready, stock) vs. cons (double taxation, formalities); compare with LLC and S-corp election. Recommend a CPA/lawyer review.
3. If proceeding: state choice (home state vs. Delaware trade-offs), articles of incorporation, registered agent, bylaws, initial board, share issuance, 83(b) awareness for founders with vesting.
4. Compliance: annual reports, board minutes, separate bank account, payroll if paying salaries.
5. Call create_document (type "plan"). General information, not legal advice — review anything binding with a lawyer. General information, not tax advice — confirm with a CPA or tax professional.

## Guardrails

- Explains double taxation and alternatives before you commit
- General information, not legal advice — review anything binding with a lawyer.
- General information, not tax advice — confirm with a CPA or tax professional.
- Draft the deliverable in your reply as a clean document the artist can copy. Use only facts the artist supplies; mark anything missing as [CONFIRM: ...] and ask at most one question at a time.
- Never invent names, credits, streaming numbers, press quotes, shows, contacts, links, dates, fees or legal facts.
- Do not send, post, publish, submit, file, register, sign or pay for anything on the artist's behalf. The artist takes every external action.
- Never ask for passwords, SSNs, bank or card numbers.
- Legal, tax and money content is general information, not professional advice; tell the artist to have a qualified professional review anything binding.

## Running in Claude

Tool names in the playbook (`create_document`) belong to the Artispreneur app and are not available here. Do the same work in the conversation instead; for directory lookups, ask the artist to search artispreneur.com/directory and paste what they find.

If the Artispreneur MCP server bundled with this plugin is connected (tools such as `get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`), you may call it: `get_skill` with slug `create-c-corp` returns the latest version of this playbook; `find_skills` matches a plain-language need to a playbook; `plan_release` and `check_release_readiness` compute release checklists from the dates and statuses the artist gives you; `get_epk_outline` returns an EPK structure per audience. The server is read-only and needs no sign-in. If it isn't connected, follow this file as written.

## Example request

> Help me decide whether to incorporate as a C-corp and walk me through it. Ask me about my revenue, partners, and goals first.
