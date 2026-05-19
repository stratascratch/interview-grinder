# Contributing to StrataScratch Skills

Thanks for your interest in contributing! Here's how to add a new skill or improve an existing one.

## Adding a New Skill

1. **Create a folder** under `skills/` with a kebab-case name:
   ```
   skills/my-new-skill/
   ├── SKILL.md       # Required
   ├── README.md      # Recommended
   ├── assets/        # Optional: reference data
   └── scripts/       # Optional: helper scripts
   ```

2. **Write your SKILL.md** with YAML frontmatter:
   ```yaml
   ---
   name: my-new-skill
   description: What this skill does and when to activate it.
   ---
   ```

3. **Update marketplace.json** — add your skill to the appropriate plugin in `.claude-plugin/marketplace.json`.

4. **Submit a PR** with a clear description of what the skill does and example usage.

## Skill Quality Guidelines

- **Description must be specific** — include trigger phrases so the agent activates reliably
- **Keep SKILL.md under 500 lines** — put reference material in separate files under `assets/`
- **Every skill must be self-contained** — no dependencies on other skills
- **Test with at least Claude Code and one other agent** before submitting
- **Include realistic examples** in your instructions
- **No copied content** — all questions, datasets, and solutions must be original

## Improving Existing Skills

1. Open an issue describing what you'd like to improve
2. Fork the repo and make your changes
3. Test the skill to verify it still works correctly
4. Submit a PR referencing the issue

## Code of Conduct

Be respectful, constructive, and focused on making data science interview prep better for everyone.
