# Boxing Rules Skill

A Claude Code skill that answers questions about boxing rules, regulations, and competition procedures using official World Boxing and Boxing Canada rule sets.

## Installation

Install this skill into your Claude Code agent with a single command:

```bash
npx skills@latest add ubaniak/boxing-rules
```

The installer will:
1. Clone this repository
2. Display available skills
3. Let you select which to install
4. Copy the skill to `~/.claude/skills/boxing-rules/`

After installation, the skill is immediately available in Claude Code agents and MCP servers.

## Usage

Ask the skill about any boxing-related topic:

- Boxing rules and regulations
- Competition procedures and bout format
- Weight categories and limits
- Scoring and judges' decisions
- Fouls, penalties, and knockdowns
- Equipment requirements
- Official roles (referees, judges, etc.)
- Canadian-specific boxing rules

**Example questions:**
- "What are the weight categories in boxing?"
- "What's the difference between a knockdown and a knockout?"
- "What fouls result in point deductions?"
- "How does the Canadian amateur boxing system differ from World Boxing?"

## Rules Sources

This skill consults two authoritative sources in order:

1. **World Boxing Competition Rules** (February 2024)  
   https://worldboxing.org/wp-content/uploads/2024/09/World-Boxing-Competition-Rules-Feb-2024-v3.99-ClEAN.pdf

2. **Boxing Canada Articles and Rules** (January 2025)  
   https://boxingcanada.org/wp-content/uploads/2025/04/Articles-and-Rules-January-2025.pdf

When the skill answers a question, it cites the specific rule numbers from these official documents so you can verify the information.

## How It Works

The skill uses a dual-source lookup system:

1. **Primary lookup**: Checks World Boxing Competition Rules
2. **Secondary overlay**: Adds Boxing Canada context and notes any differences
3. **Citations**: Every answer includes source citations (e.g., `[World Boxing – Rule 8.6.2]`)
4. **Flags differences**: When Canadian rules differ from World Boxing rules, they're clearly marked

## Documentation

- `SKILL.md` — Technical skill definition and answer format requirements
- `CLAUDE.md` — Architecture and maintenance guide for future development
- `references/world-boxing-rules.md` — Full World Boxing Competition Rules
- `references/boxing-canada-rules.md` — Full Boxing Canada Articles and Rules

## License

MIT
