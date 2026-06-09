# AXIA Design Skill

**Production-grade UI/UX design intelligence for Claude Code.**

AXIA Design is a Claude Code skill that transforms how you build frontend interfaces. Instead of generating generic, cookie-cutter UI, it establishes intentional aesthetic direction first — then delivers complete, implementation-ready code with a coherent design system.

---

## What It Does

- **Design direction first** — Identifies purpose, picks a tonal voice (clean SaaS, dark premium, bold editorial, brutalist, etc.), and commits to it before writing a single line of code
- **Full design system** — Generates typography tokens, color palettes (3-layer: base → surface → accent), spacing scales, and radius values before components
- **Layout intelligence** — Context-aware layouts based on use case: landing pages, dashboards, auth flows, pricing, docs, portfolios, e-commerce
- **Complete component standards** — Buttons, forms, cards, navigation, and data display with all states covered (hover, focus, active, disabled, loading, empty, error)
- **Motion system** — Aesthetic-matched animation tokens and patterns that communicate rather than decorate
- **Accessibility built-in** — WCAG contrast, keyboard navigation, reduced-motion support baked into every output
- **Stack-aware** — Tailored implementation for Next.js + Tailwind + shadcn/ui, React, Vue/Nuxt, and plain HTML/CSS

---

## Supported Aesthetics

| Voice | Feel | Inspired By |
|---|---|---|
| `clean-saas` | Minimal, high-signal, professional | Linear, Vercel, Raycast |
| `bold-editorial` | Strong type, high contrast, magazine | NYT, The Pudding |
| `dark-premium` | Dark-first, layered depth, glass | Resend, Clerk |
| `playful-brand` | Organic, vibrant, personality | Lemon Squeezy, Mobbin |
| `brutalist` | Raw structure, monospace, tension | brutalistwebsites.com |
| `retro-tech` | CRT, terminal, warm amber/green | — |
| `glassmorphic` | Frosted layers, blur as structure | — |
| `maximalist` | Dense, layered, decorative | — |

---

## Supported Stacks

- **Next.js + Tailwind + shadcn/ui** (primary)
- **React + Tailwind** (cva + Radix primitives)
- **Vue / Nuxt** (Nuxt UI / Headless UI)
- **Plain HTML + CSS** (custom properties + clamp)

---

## Installation

### Option A — Install directly to Claude Code (recommended)

```bash
# Copy SKILL.md into your Claude skills directory
# macOS / Linux
cp skills/axia-design/SKILL.md ~/.claude/skills/axia-design.md

# Windows (PowerShell)
Copy-Item skills\axia-design\SKILL.md "$env:USERPROFILE\.claude\skills\axia-design.md"
```

### Option B — Project-level install

```bash
mkdir -p .claude/skills
cp skills/axia-design/SKILL.md .claude/skills/axia-design.md
```

Restart Claude Code. The skill activates automatically when you ask for any UI work.

---

## Usage

Just describe what you want naturally:

```
Build a landing page for my developer tools SaaS
```

```
Design a dashboard for a fintech app — dark mode, dense data
```

```
Make this component look more premium
```

```
Add scroll animations to this hero section
```

The skill will state its design direction, establish tokens, then generate complete code.

---

## What It Won't Do

- Generate purple gradient heroes on white backgrounds
- Default to centered hero + three equal cards
- Use Inter or Space Grotesk as the "safe" choice
- Ship components with missing states (loading, empty, error)
- Ignore accessibility or dark mode

---

## License

MIT — free to use, modify, and distribute.

---

## Contributing

PRs welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

Built by [AXIA](https://github.com/AXIAbuilt).

## Pro

**[Get AXIA Design Pro — $9](https://axiabuilt.gumroad.com/l/pbbjqy)**

Includes brand audit mode, Figma token export, 20+ extended aesthetics, micro-interaction library, fluid type system, multi-page coherence check, and component spec output. One-time purchase, lifetime access.
