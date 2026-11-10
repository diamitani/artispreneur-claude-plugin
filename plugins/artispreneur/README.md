# Artispreneur for Claude

Artispreneur gives independent artists, managers and small labels a music-business team inside Claude. This plugin bundles 48 skills (EPKs, artist bios, release plans, royalties and PRO registration, business setup, budgets, content, booking and outreach), 7 desk agents that act like departments of an artist's team, and a connection to the free, read-only Artispreneur MCP server.

Every skill drafts in the conversation from facts the artist supplies. Nothing in this plugin sends email, posts, files paperwork, registers works, signs, or pays. Legal, tax and money content is general information, not professional advice.

## What it contains

- `skills/`: 48 skills, one folder per skill with a `SKILL.md`. They load in Claude Code, claude.ai chat and Cowork.
- `agents/`: 7 desk subagents. They load in Claude Code and Cowork; claude.ai chat ignores agents.
- `.mcp.json`: one remote MCP server, `artispreneur`, at https://www.artispreneur.com/mcp (Streamable HTTP, no authentication).
- No hooks, scripts, executables, or local servers.

## What it connects to and sends

The only network endpoint is https://www.artispreneur.com/mcp. It exposes 9 read-only tools (`get_pricing`, `check_release_readiness`, `list_desks`, `list_skills`, `get_skill`, `get_desk_prompt`, `plan_release`, `find_skills`, `get_epk_outline`) and the desk starter prompts, server version 1.2.1. Claude sends it only the arguments of a tool call, such as a skill slug, a release date, readiness statuses or an EPK audience. The server needs no account, stores nothing from the call, and cannot read or change any Artispreneur account. Do not put personal details in tool arguments.

## Install

Claude Code, from this public marketplace:

```bash
claude plugin marketplace add diamitani/artispreneur-claude-plugin
claude plugin install artispreneur@artispreneur
```

Claude Code, for one session from a local copy: `claude --plugin-dir ./plugins/artispreneur`.

claude.ai or the Claude desktop app: Customize > Plugins > Add > Upload plugin, with a zip of this folder. Or add the MCP server alone as a custom connector with the URL above.

## Desk agents

| Agent | Desk | Focus |
| --- | --- | --- |
| `artispreneur:home-base` | Home Base | Your HQ: priorities, planning, and anything cross-team. |
| `artispreneur:business-team` | Business Team | Business plan, contracts, split sheets, budgets, registration. |
| `artispreneur:press-team` | Press Team | Bios, EPKs, press releases, and media pitches. |
| `artispreneur:release-team` | Release Team | Rollouts, distribution, and royalty registration. |
| `artispreneur:booking-team` | Booking Team | Venues, tours, and booking pitches from the live directory. |
| `artispreneur:content-team` | Content Team | Captions, threads, video concepts, and newsletters. |
| `artispreneur:outreach-team` | Outreach Team | Pitch emails for bookings, press and partnerships, sent from your own inbox, plus submissions and follow-ups. |

## Skills

| Skill | Name | Desk |
| --- | --- | --- |
| `create-an-epk` | EPK Builder | Press Team |
| `create-an-artist-bio` | Artist Bio Writer | Press Team |
| `create-brand-logo` | Brand Logo | Business Team |
| `write-brand-guidelines` | Brand Guidelines | Business Team |
| `create-split-sheet-agreement` | Split Sheet Agreement | Business Team |
| `license-music` | Music Licensing Brief | Business Team |
| `get-ein` | EIN Registration | Business Team |
| `create-llc` | LLC Formation | Business Team |
| `create-c-corp` | C-Corp Formation | Business Team |
| `open-business-bank-account` | Business Bank Account | Business Team |
| `manage-business-expenses` | Expense Manager | Business Team |
| `file-business-taxes` | Business Tax Filing | Business Team |
| `track-royalties-on-dsps` | Royalty Tracker | Release Team |
| `write-a-business-plan` | Business Plan | Home Base |
| `register-with-pro` | PRO Registration | Release Team |
| `register-tracks-with-pro` | Track Registration | Release Team |
| `claim-tracks-with-pro` | Unclaimed Royalties | Release Team |
| `set-up-dsp` | DSP Setup | Release Team |
| `release-music-with-dsp` | Release Engine | Release Team |
| `extract-metadata-from-track` | Metadata Extractor | Release Team |
| `transcribe-lyrics` | Lyric Transcriber | Content Team |
| `upload-track-to-catalogue` | Catalog Upload | Release Team |
| `create-content-calendar` | Content Calendar | Content Team |
| `generate-social-media-content` | Social Content Pack | Content Team |
| `create-lyric-video` | Lyric Video | Content Team |
| `write-music-video-treatment` | Video Treatment | Content Team |
| `upload-music-video-to-youtube` | YouTube Upload | Content Team |
| `analyze-social-media-engagement` | Engagement Audit | Content Team |
| `create-merch-designs` | Merch Designs | Content Team |
| `set-up-merch-drop-shipping` | Merch Fulfillment | Business Team |
| `add-music-to-collaborative-playlist` | Playlist Pitching | Booking Team |
| `artist-profile` | Artist Profile | Home Base |
| `artist-goals` | Goal Setting | Home Base |
| `weekly-win-plan` | Weekly Win Plan | Home Base |
| `brand-positioning` | Brand Positioning | Content Team |
| `pr-campaign` | PR Campaign | Press Team |
| `media-outreach` | Media Pitching | Outreach Team |
| `playlist-outreach` | Playlist Curator Pitching | Outreach Team |
| `booking-outreach` | Booking Outreach | Outreach Team |
| `directory-search` | Industry Contact Finder | Booking Team |
| `distribution-readiness` | Distribution Readiness | Release Team |
| `royalty-readiness` | Royalty Readiness | Business Team |
| `budget-planning` | Budget & Runway | Business Team |
| `contract-intake` | Contract Explainer | Business Team |
| `legal-business-checklist` | Business Setup Checklist | Business Team |
| `knowledge-ingestion` | Teach Your Agent | Home Base |
| `build-an-agent` | Build an Agent | Home Base |
| `build-a-skill` | Build a Skill | Home Base |

## Support

Website: https://www.artispreneur.com. Developer docs: https://www.artispreneur.com/developers. Support: https://www.artispreneur.com/support. Privacy: https://www.artispreneur.com/legal/privacy. Terms: https://www.artispreneur.com/legal/terms.

This folder is generated from the Artispreneur catalog by `scripts/build-claude-plugin.ts`; edit the catalog, not these files.
