# Artispreneur Claude plugins

Public Claude Code marketplace for [Artispreneur](https://www.artispreneur.com): music-business skills and desk agents for independent artists, managers and labels.

This repository lists **56 plugins**: the full `artispreneur` bundle (48 skills and 7 desk agents) plus a searchable plugin for each skill and each desk. Every plugin connects to the free, read-only Artispreneur MCP server at https://www.artispreneur.com/mcp. Skills draft in the conversation from facts you supply. Nothing here sends email, posts, files paperwork, registers works, signs, or pays. Legal, tax and money content is general information, not professional advice.

## Install (Claude Code)

```bash
claude plugin marketplace add diamitani/artispreneur-claude-plugin
claude plugin install artispreneur@artispreneur
```

Install a single skill or desk the same way, for example:

```bash
claude plugin install artispreneur-create-llc@artispreneur
```

Then restart Claude Code or start a new session so the skills and agents load.

## What's in the marketplace

- `artispreneur` — all 48 public skills, 7 desk agents (Home Base, Business, Press, Release, Booking, Content, Outreach), and the public MCP server.
- 48 skill plugins — `artispreneur-<skill-slug>`, for example `artispreneur-create-llc` and `artispreneur-create-an-epk`.
- 7 desk plugins — `artispreneur-home-base`, `artispreneur-business-team`, `artispreneur-press-team`, `artispreneur-release-team`, `artispreneur-booking-team`, `artispreneur-content-team`, `artispreneur-outreach-team`.

On claude.ai or the Claude desktop app: Customize > Plugins > Add > Upload plugin, with a zip of one folder under `plugins/`. Or add the MCP server alone as a custom connector at https://www.artispreneur.com/mcp (no sign-in).

Listings in Anthropic's official plugin directory are not submitted from this repository yet.

## License

Copyright (c) 2026 Artispreneur Inc. All rights reserved. See [LICENSE](LICENSE). The `license` field on each plugin is `UNLICENSED`. Use is governed by the [Artispreneur Terms of Service](https://www.artispreneur.com/legal/terms).

## Support

Website: https://www.artispreneur.com. Developer docs: https://www.artispreneur.com/developers. Support: https://www.artispreneur.com/support. Privacy: https://www.artispreneur.com/legal/privacy.
