<p align="center">
  <img src="assets/cover.png" alt="StrataScratch Interview Grinder" width="600">
</p>

# Interview Grinder

An agent skill that generates complete data science interview questions — exactly as they appear on the [StrataScratch](https://www.stratascratch.com) platform. Title, question, and dataset preview, ready to solve.

Compatible with **Claude Code**, **OpenAI Codex**, **Gemini CLI**, **Cursor**, and other agents that support the open [Agent Skills](https://agentskills.io) standard.

## What It Does

The Interview Grinder creates original, interview-ready questions with:

- **Title** — Short, descriptive name (e.g., "Top Salaries by Department")
- **Question** — Business-framed problem with clear output requirements
- **Dataset Preview** — Table schemas with sample rows, exactly as shown on the platform

Questions are calibrated against a bank of 100 real StrataScratch questions for style, difficulty, and structure — but every output is 100% original.

## Quick Start

```bash
# npx (any agent)
npx skills add gencay-strata/interview-grinder

# Claude Code
/plugin marketplace add gencay-strata/interview-grinder
```

Or clone manually:

```bash
git clone https://github.com/gencay-strata/interview-grinder.git
cp -r skills/strata-interview-grinder ~/.claude/skills/
```

## Usage

Just ask naturally:

```
Generate an interview question
```

```
Give me a hard SQL question about customer churn
```

```
Grind a question about window functions
```

The skill activates automatically when it detects interview question creation intent.

### Hotkeys

After each question, use these shortcuts:

| Key | Action |
|-----|--------|
| **Q** 🔄 | Generate a brand new question |
| **R** ✏️ | Revise a specific section |
| **D** 📊 | Regenerate dataset with different data |

## Interview Mode

This skill operates in **interview mode** — it presents the question and data, you solve it. Solutions, hints, and edge case explanations are never shown. Edge cases are silently embedded in the dataset for you to discover.

## Skill Format

Each skill follows the open [Agent Skills](https://agentskills.io) standard:

```
skills/strata-interview-grinder/
├── SKILL.md       # Instructions and metadata
├── README.md      # Documentation
└── assets/        # Reference data (question bank CSV)
```

## Links

- [StrataScratch Platform](https://www.stratascratch.com)
- [Agent Skills Specification](https://agentskills.io)
- [Using Skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude)

## License

Released under the [Apache 2.0 License](./LICENSE).
