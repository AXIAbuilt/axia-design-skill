# Contributing to AXIA Design Skill

Thank you for your interest in contributing. This project is a Claude Code skill — contributions that improve design quality, coverage, or stack support are welcome.

## What We're Looking For

- New aesthetic voices with real examples and token sets
- Stack-specific implementation improvements (Svelte, Solid, Angular, etc.)
- Additional layout patterns for new use cases
- Accessibility improvements
- Anti-pattern additions based on real observed issues

## What We're Not Looking For

- Generic "clean up" PRs without specific rationale
- Adding Inter/Space Grotesk back as defaults
- Framework-agnostic advice that dilutes stack-specific guidance

## How to Contribute

1. Fork the repository
2. Edit `skills/axia-design/SKILL.md` directly — this is the single source of truth
3. Test your changes by installing locally and using Claude Code on real UI tasks
4. Open a PR with a clear description of what changed and why

## Skill File Structure

The `SKILL.md` file uses YAML frontmatter followed by markdown content:

```markdown
---
name: skill-name
description: One-sentence trigger description used by Claude to decide when to activate
---

# Skill content here
```

The `description` field is critical — it determines when Claude auto-activates the skill. Keep it specific and action-oriented.

## Testing

Before submitting a PR, test with at least these prompts:
- "Build a landing page for [product type]"
- "Design a dashboard"  
- "Add dark mode to this component"
- "Make this more accessible"

The output should reflect the guidance in your changes — not previous behavior.
