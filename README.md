# Juicify

Turn experience into reusable insight.

Juicify is a Claude Code plugin with two complementary skills for extracting and crystallizing knowledge:

- **skill-juice** — Extract design wisdom from any skill or plugin through a 6-lens analysis framework
- **work-juice** — Crystallize your completed work into structured case study reports

## Installation

```bash
# Add the marketplace
/plugin marketplace add hminnnnnn/juicify

# Install the plugin
/plugin install juicify
```

## Skills

### skill-juice

Analyze any skill to understand *why* it works, not just *what* it does. Extracts insights across 6 lenses:

| Lens | What it extracts |
|------|-----------------|
| Design Philosophy | Worldview, core principles, root problem |
| Systems Thinking | Structural patterns, feedback loops, separation of concerns |
| Engineering Techniques | Reusable techniques with source citations |
| Prompt Design | LLM instruction patterns, Theory of Mind usage |
| User Experience | Input flexibility, feedback loops, error handling |
| Apply to Your Work | Concrete, actionable insights for your current project |

**Usage:**

```bash
/juicify:skill-juice brainstorming          # deep mode (default)
/juicify:skill-juice brainstorming quick    # quick mode (3 lenses)
/juicify:skill-juice ~/.claude/skills/my-skill deep
/juicify:skill-juice https://github.com/someone/skill-repo
```

**Output:** Juice Note saved to `docs/juice-notes/YYYY-MM-DD-{skill-name}.md` + session summary.

### work-juice

Turn completed work cycles (issue → analysis → improvement → verification) into structured case study reports.

**Usage:**

```bash
/juicify:work-juice latest    # Report on the most recent case
/juicify:work-juice select    # Choose from multiple cases in the session
/juicify:work-juice           # Interactive mode selection
```

**Output:** Case study report saved to `docs/reports/YYYY-MM-DD-{topic}.md`

**Report structure:** Summary → Discovery → Root Cause → Options Considered → Implementation → Verification → Lessons Learned

## Why Juicify?

Most people install a skill, use it, and move on. That's borrowing someone else's tool. Juicify helps you **absorb the wisdom behind the tool** — why was it designed this way? What thinking patterns are baked in?

Similarly, most work gets done and forgotten. Juicify helps you **turn every work cycle into a reusable lesson** — what did you discover? What would you do differently?

## Multilingual Support

Both skills respond in the user's language. The skill body is written in Korean, but output adapts to your conversation language.

## License

MIT
