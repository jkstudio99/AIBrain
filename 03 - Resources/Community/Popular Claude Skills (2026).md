---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/community
  - topic/claude
  - topic/skills
related:
  - "[[03 - Resources/Community/Community & Resources]]"
  - "[[03 - Resources/Claude Integration/MCP Tools & Skills]]"
  - "[[MOCs/Obsidian Claude Ecosystem MOC]]"
---

# Popular Claude Skills (2026)

> [!note]
> Checked on April 16, 2026. "Popular" here is an inference from current Claude Code docs plus visible GitHub traction in major skill marketplaces, not an official Anthropic ranking.

## What Counts As "Popular" In 2026
- Skills bundled directly in Claude Code are the safest default picks because Anthropic documents and ships them.
- Marketplace skills with strong GitHub adoption are the best signal for broader community usage.
- For this vault, relevance matters more than raw popularity, so Obsidian-friendly skills are called out separately.

## Tier 1: Official Claude Code Skills

These are built into current Claude Code and documented by Anthropic:

| Skill | Why it is popular | Best use |
|------|--------------------|----------|
| `/batch` | High-leverage for large codebase changes with parallel worktrees | Big migrations, broad refactors, multi-PR work |
| `/claude-api` | Pulls in Claude API references automatically when SDK usage appears | API integration, SDK work, tool use, structured outputs |
| `/debug` | Purpose-built troubleshooting skill with session debug log support | Claude Code issues, weird tool behavior, local debugging |
| `/loop` | Lets Claude run recurring checks while a session stays open | Long deploys, watch tasks, repeated maintenance checks |
| `/simplify` | Built-in quality/reuse pass that can review and fix changed code | Cleanup, reuse, efficiency, post-implementation refinement |

## Tier 2: Strong Community Skill Marketplaces

### 1. daymade/claude-code-skills
- GitHub stars: **845** on April 16, 2026
- Positioning: large general-purpose marketplace with **48 production-ready skills**
- Best popular picks:
  - `skill-creator`: meta-skill for building, validating, and packaging your own skills
  - `prompt-optimizer`: turns vague prompts into structured specifications using EARS methodology
  - `qa-expert`: QA testing infrastructure with autonomous execution
  - `docs-cleaner`: consolidates redundant documentation into cleaner authoritative docs
  - `claude-md-progressive-disclosurer`: trims `CLAUDE.md` bloat by moving details into references

### 2. mhattingpete/claude-skills-marketplace
- GitHub stars: **548** on April 16, 2026
- Positioning: software engineering workflow marketplace
- Best popular picks:
  - `feature-planning`: breaks feature requests into implementable plans
  - `test-fixing`: groups and fixes failing tests systematically
  - `git-pushing`: stages, commits, and pushes with workflow automation
  - `review-implementing`: applies PR/code review feedback systematically
  - `architecture-diagram-creator`, `flowchart-creator`, `technical-doc-creator`: useful for docs-heavy engineering workflows

### 3. netresearch/claude-code-marketplace
- GitHub stars: **28** on April 16, 2026
- Positioning: more niche than the two marketplaces above, but useful for specialized stacks
- Strongest fit:
  - TYPO3, PHP, Go, Docker, Jira, security, and documentation-heavy teams
- Best viewed as a specialist marketplace, not a general starter pack

## Best Skills For This Vault

If the goal is to improve this Obsidian + Claude setup specifically, these are the highest-value skills:

### Already Installed And High Value
- `obsidian-markdown`
- `obsidian-cli`
- `obsidian-bases`
- `json-canvas`
- `defuddle`

### Best Additional Skills To Consider
- `docs-cleaner`
  - Good for consolidating overlapping resource notes as this vault grows
- `claude-md-progressive-disclosurer`
  - Good when `CLAUDE.md` or other control docs get too large
- `prompt-optimizer`
  - Good for turning rough prompt ideas into reusable command-quality prompts
- `feature-planning`
  - Good if this vault starts managing more software projects directly
- `flowchart-creator` or `architecture-diagram-creator`
  - Good if you want richer documentation and visual explanation workflows

## Suggested Adoption Order
1. Keep using the installed Obsidian-focused skills first.
2. Add one documentation skill: `docs-cleaner`.
3. Add one prompt quality skill: `prompt-optimizer`.
4. Add one planning or engineering skill if project work grows: `feature-planning`.
5. Add diagram/documentation skills only when you actually need them.

## Notes For This Vault
- For note quality, the most important skills are still `obsidian-markdown` and `obsidian-cli`.
- For long-term maintainability, `docs-cleaner` and `claude-md-progressive-disclosurer` are the most interesting 2026 additions.
- For general coding outside the vault, the strongest "default" set in 2026 is `/batch`, `/simplify`, `feature-planning`, `test-fixing`, and `prompt-optimizer`.

## Sources
- [Claude Code commands](https://code.claude.com/docs/en/commands)
- [Create plugins](https://code.claude.com/docs/en/plugins)
- [Plugin marketplaces](https://code.claude.com/docs/en/plugin-marketplaces)
- [daymade/claude-code-skills](https://github.com/daymade/claude-code-skills)
- [mhattingpete/claude-skills-marketplace](https://github.com/mhattingpete/claude-skills-marketplace)
- [netresearch/claude-code-marketplace](https://github.com/netresearch/claude-code-marketplace)
