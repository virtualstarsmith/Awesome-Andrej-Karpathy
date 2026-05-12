# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an **awesome-list** repository (`Awesome-Andrej-Karpathy`) — a curated, bilingual (English + Chinese) map of Andrej Karpathy's open-source projects and 200+ community derivatives. It follows standard `awesome-*` conventions (single-line bullet entries, categorized sections, emoji legend).

## Repository Structure

- `README.md` — English awesome-list (primary)
- `README.zh-CN.md` — Chinese translation (parallel structure, same sections)
- `CONTRIBUTING.md` — Inclusion criteria, entry format, PR process
- `SECURITY.md` — Scope of review for listed projects
- `CODE_OF_CONDUCT.md` — Contributor Covenant
- `.github/ISSUE_TEMPLATE/` — `add_skill.yml`, `remove_skill.yml`, `update_skill.yml`

## Inclusion Criteria

Every listed project must meet one of three bars (see CONTRIBUTING.md):
- **A — Official**: By Karpathy himself
- **B — Direct derivative**: README explicitly says *inspired by / port of / based on* a Karpathy work
- **C — Concept derivative**: Explicitly cites a named Karpathy concept (Software 2.0/3.0, LLM OS, Vibe Coding, etc.)

## Entry Format

```
- [author/repo](https://github.com/author/repo) - One-line description ending with a period.
```

Prefix with the appropriate emoji from the Legend section. Add 🇨🇳 for Chinese-language projects. Multi-language ports go in their dedicated section.

## Editing Rules

- **One entry per PR** (preferred). Title format: `Add: author/repo` or `Update: author/repo`.
- New sub-categories require a matching idea seed in the *Concepts & Manifestos* section.
- Keep EN and CN READMEs in sync — structural changes must be mirrored.
- Star counts, links, and descriptions drift; update PRs are welcome.
- Dead links or archived repos should be flagged with the `remove` label.

## Bilingual Conventions

- `README.md` is authoritative. `README.zh-CN.md` is a parallel translation.
- Section anchors differ between languages (e.g., `#llm-wiki` vs `#llm-wiki-zh`).
- The Chinese version uses `-zh` suffixed anchors for duplicate section names.

## License

CC0 1.0 Universal — public domain dedication.
