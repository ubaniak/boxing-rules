# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a Claude Code skill that answers questions about boxing rules, regulations, and competition procedures. It provides structured access to two official rule sets: World Boxing Competition Rules and Boxing Canada Articles and Rules.

Not a traditional software project — no build, test, or lint commands.

## Project Structure

```
boxing-rules/
├── SKILL.md                           # Skill definition & usage instructions
├── references/
│   ├── world-boxing-rules.md          # World Boxing Competition Rules (Feb 2024)
│   └── boxing-canada-rules.md         # Boxing Canada Articles & Rules (Jan 2025)
└── CLAUDE.md                          # This file
```

## Skill Architecture

The skill uses a two-source lookup system:

1. **Primary source**: `references/world-boxing-rules.md` (World Boxing Competition Rules, Feb 2024)
2. **Secondary source**: `references/boxing-canada-rules.md` (Boxing Canada rules, Jan 2025)

**Lookup order**: Always check World Boxing first, then overlay with Boxing Canada context. Flag differences when they exist.

**Citation format**: `[World Boxing – Rule X.X.X]` or `[Boxing Canada – Rule X.X.X]`

## When to Use This Skill

This skill is invoked whenever a user asks about:
- Boxing rules or regulations
- Competition procedures
- Equipment requirements
- Weight categories and limits
- Scoring and judges' decisions
- Fouls and penalties
- Knockdowns and knockout procedures
- Officials and referee roles
- Bout format and structure
- Canadian-specific boxing rules

## Maintaining Reference Files

The reference Markdown files (`references/world-boxing-rules.md` and `references/boxing-canada-rules.md`) contain the full text of official rule documents. Structure is rule-number-based to enable accurate citations.

**When updating**:
- Preserve rule numbering structure for citation accuracy
- Maintain article groupings from original documents
- Add date notes if updating with newer rule versions
- Clearly mark any Canadian-specific modifications or exceptions

## Key Files Reference

| File | Purpose | Source |
|------|---------|--------|
| `SKILL.md` | Defines skill behavior, answer format, citation rules | Instructor for the skill itself |
| `references/world-boxing-rules.md` | World Boxing Competition Rules (Feb 2024) | https://worldboxing.org/wp-content/uploads/2024/09/World-Boxing-Competition-Rules-Feb-2024-v3.99-ClEAN.pdf |
| `references/boxing-canada-rules.md` | Boxing Canada Articles & Rules (Jan 2025) | https://boxingcanada.org/wp-content/uploads/2025/04/Articles-and-Rules-January-2025.pdf |
