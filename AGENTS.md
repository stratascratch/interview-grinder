# AGENTS.md

This file provides guidance to AI coding agents (Claude Code, Codex, Cursor, Copilot, etc.) when working with code in this repository.

## Repository Purpose

A collection of agent skills for data science interview preparation, maintained by [StrataScratch](https://www.stratascratch.com).

## Structure

```
stratascratch-skills/
├── .claude-plugin/
│   └── marketplace.json      # Plugin registry for Claude Code
├── skills/
│   └── {skill-name}/
│       ├── SKILL.md           # Required: skill definition
│       ├── README.md          # Recommended: human-readable docs
│       └── assets/            # Optional: reference data (CSVs, etc.)
├── template/
│   └── SKILL.md               # Starter template for new skills
├── README.md
├── CONTRIBUTING.md
├── AGENTS.md
└── LICENSE
```

## Conventions

- **Skill directories**: kebab-case (e.g., `strata-interview-grinder`)
- **SKILL.md**: Always uppercase, always this exact filename
- **Frontmatter**: Every SKILL.md must have `name` and `description` in YAML frontmatter
- **Assets**: Reference data goes in `assets/` within the skill folder
- **Descriptions**: Must include trigger phrases for reliable agent activation

## Adding a New Skill

1. Create `skills/{skill-name}/SKILL.md` with valid frontmatter
2. Add a `README.md` with usage examples
3. Register the skill in `.claude-plugin/marketplace.json`
4. Update the skills table in the root `README.md`

## Quality Standards

- Skills must be self-contained — no cross-skill dependencies
- Questions, datasets, and solutions must be original — never copied
- Keep SKILL.md under 500 lines; put reference material in `assets/`
- Test with at least two different agent platforms before merging
