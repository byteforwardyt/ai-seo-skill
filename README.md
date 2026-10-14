# AI SEO Skill

A free skill that tells an AI agent how to make a page, listing, or brand findable on the search surface that matters, without invented statistics or retired tricks.

## What it is

This is a set of instructions an agent loads when you ask for search visibility. It is not an SEO tool, a rank tracker, or a chatbot you sign up for. There is no server, account, or API key. The skill runs no code.

The instructions are in [skills/ai-seo-skill/SKILL.md](skills/ai-seo-skill/SKILL.md). The files in `skills/ai-seo-skill/references/` are the detail the agent loads for one surface at a time. This repository is also an [Agent Plugin](https://agent-plugins.org), so a client that installs plugins can load the same folder.

It is free under the MIT license.

## What it does

When the skill is active, the agent is told to:

- Name the surface first. Google, Maps, YouTube, Amazon, and the App Store do not share one algorithm.
- Inspect the URL if it can, instead of auditing a domain from its name.
- Load one or two reference files, not a stack of unrelated guides.
- Separate a platform requirement, documented platform guidance, and industry practice.
- Follow Google's own guide for AI Overviews: those features use normal Search systems, and there is no special schema, chunk-size target, or `llms.txt` file to add.
- Skip HowTo rich results, because Google removed them, and not promise FAQ rich results to ordinary sites.
- Refuse keyword stuffing, fake reviews, doorway pages, and schema that describes content the page does not show.
- Produce a scorecard or a 90-day plan only when you ask for one.

## Why you need it

Search advice online is full of numbers that were never measured and tactics Google has already turned off. An agent that has read that advice will repeat it with confidence: a 40-word block after every heading, a HowTo schema, a voice-search statistic from an old forecast, a percentage lift from a vendor's own test.

That wastes the week you spend implementing it. You need the agent to say which surface is broken, which claim is just a habit, and which change is worth making on this page. This skill is that constraint. It does not rank the page for you. The agent still has to look.

## What this version corrects

The skill you may already have installed tells the agent to load `references/` files that were not in the installed copy. It also states specific percentages, word-count windows, and rich-result tactics that do not hold up.

This repository supplies the missing references and removes those claims. It is an original rewrite. It covers the same search surfaces as the public [Attainment Labs skill](https://github.com/attainmentlabs/ai-seo-skill), and it does not include that repository's files. Those files were not republished.

## Install

```bash
npx skills add byteforwardyt/ai-seo-skill
```

Add `-g` to install it for every project. The [skills CLI](https://github.com/vercel-labs/skills) copies the skill into the folder each detected agent reads.

To install it by hand, copy `skills/ai-seo-skill` into the agent's skills directory and start a new chat.

| Agent | This project | Every project |
| --- | --- | --- |
| Cursor | `.agents/skills/` or `.cursor/skills/` | `~/.agents/skills/` or `~/.cursor/skills/` |
| Claude Code | `.claude/skills/` | `~/.claude/skills/` |
| Codex, Cline, and other agents that read `.agents/skills/` | `.agents/skills/` | `~/.agents/skills/` |
| GitHub Copilot | `.agents/skills/` | `~/.copilot/skills/` |

### Install in Claude Code

On Claude Code 2.1.275 or later:

```text
/plugin install ai-seo-skill --marketplace byteforwardyt/ai-seo-skill
```

On an older Claude Code:

```bash
claude plugin marketplace add byteforwardyt/ai-seo-skill
claude plugin install ai-seo-skill@ai-seo-skill
```

### Install the plugin in VS Code

Open the Command Palette, run **Chat: Install Plugin From Source**, and paste:

```text
https://github.com/byteforwardyt/ai-seo-skill
```

## Try it

- Audit this URL for the search surfaces that matter. Say what is broken, what is fine, and what you could not check.
- Which search surfaces should this business prioritize, and which should it ignore?
- Rewrite this page for the searcher. Flag anything that would be keyword stuffing or a retired rich-result trick.

## What's in this repo

```text
plugin.json                         Plugin identity
.codex-plugin/plugin.json           Codex-compatible listing fallback
.claude-plugin/marketplace.json     Claude Code marketplace entry
skills/ai-seo-skill/SKILL.md        The skill
skills/ai-seo-skill/references/     One file per surface, loaded on demand
```

There is nothing to build and nothing to configure.

## License

[MIT](LICENSE). Copyright (c) 2026 Byte Forward.
