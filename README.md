<p align="center">
  <img src="assets/cover.png" alt="StrataScratch Interview Grinder" width="600">
</p>

# StrataScratch Skills

Skills are folders of instructions, scripts, and resources that AI agents load dynamically to improve performance on data science interview preparation tasks. Each skill teaches the agent how to complete a specific task in a repeatable way — from generating interview questions to creating datasets with edge cases.

> **Note:** These skills follow the open [Agent Skills](https://agentskills.io) standard and are compatible with Claude Code, OpenAI Codex, Gemini CLI, Cursor, and other agent platforms.

## About This Repository

This repository contains StrataScratch's official collection of agent skills for data science interview preparation. These skills power the workflows behind [StrataScratch](https://www.stratascratch.com) — the platform where data scientists practice real interview questions from top tech companies.

### Available Skills

| Skill | Description |
|-------|-------------|
| [strata-interview-grinder](./skills/strata-interview-grinder/) | Generates complete data science interview questions with datasets in platform interview mode — title, question, and data preview, ready to solve |

## Quick Start

### Claude Code (Plugin Marketplace)

```bash
# Register the marketplace
/plugin marketplace add stratascratch/skills

# Install all skills
/plugin install interview-skills@stratascratch-skills
```

### npx skills CLI

```bash
# Install all skills
npx skills add stratascratch/skills

# Install a specific skill
npx skills add stratascratch/skills --skill strata-interview-grinder
```

### Manual Installation

```bash
# Clone and copy to your skills directory
git clone https://github.com/stratascratch/skills.git
cp -r skills/strata-interview-grinder ~/.claude/skills/
```

After installing, just describe what you want in plain English:

- *"Generate an interview question about window functions"*
- *"Give me a hard SQL question about customer retention"*
- *"Grind a question"*

The agent will automatically detect and use the right skill.

## Skill Format

Each skill is a self-contained folder:

```
skill-name/
├── SKILL.md          # Instructions and metadata (required)
├── assets/           # Reference data, CSVs (optional)
└── scripts/          # Helper scripts (optional)
```

The `SKILL.md` file contains YAML frontmatter (name + description) followed by the instructions the agent follows when the skill is active. For the full specification, see the [Agent Skills Spec](https://agentskills.io).

## Creating Custom Skills

Want to contribute a skill? Use the [template](./template/) as a starting point:

```yaml
---
name: my-skill-name
description: A clear description of what this skill does and when to use it.
---

# My Skill Name

Instructions for the agent go here...
```

See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

## Links

- [StrataScratch Platform](https://www.stratascratch.com)
- [Agent Skills Specification](https://agentskills.io)
- [Using Skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude)
- [Creating Custom Skills](https://support.claude.com/en/articles/12512198-creating-custom-skills)

## License

Skills in this repository are released under the [Apache 2.0 License](./LICENSE) unless otherwise noted in individual skill directories.
