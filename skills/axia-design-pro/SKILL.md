---
name: axia-design-pro
description: Pro-tier UI/UX design intelligence — everything in axia-design plus advanced brand auditing, Figma token export, 20+ extended aesthetics, micro-interaction library, responsive fluid type system, design critique mode, and multi-page coherence checks. Activates for any UI/UX request when the user has the Pro skill installed.
---

# AXIA Design Pro Skill

Everything in [AXIA Design](../axia-design/SKILL.md), plus the capabilities below. Pro features activate automatically based on context.

---

## Pro Feature 1 — Brand Audit Mode

Trigger: *"audit this UI"*, *"review this design"*, *"what's wrong with this"*

Analyze existing UI against these dimensions and score each 1–5:

| Dimension | What to Check |
|---|---|
| **Token Consistency** | Are spacing, color, radius, and type values consistent or arbitrary? |
| **Hierarchy** | Is there a clear visual entry point per section? Does the eye know where to go? |
| **State Coverage** | Are hover, focus, active, disabled, loading, empty, error states all present? |
| **Motion Coherence** | Do animations match the aesthetic? Are durations consistent? |
| **Accessibility** | Contrast ratios, keyboard nav, touch targets, ARIA usage |
| **Dark Mode** | Is it a real dark mode or just inverted colors? |
| **Mobile Quality** | Does the 375px layout feel designed or just squeezed? |
| **Brand Distinctiveness** | Could this belong to any company, or is it unmistakably this product? |

Output format:
```
BRAND AUDIT
──────────────────────────────
Token Consistency    ████░  4/5  Minor: 3 arbitrary px values found
Hierarchy            ███░░  3/5  Hero has no clear focal point
State Coverage       ██░░░  2/5  Missing: loading, empty, error on 4 components
Motion Coherence     █████  5/5  Clean, consistent
Accessibility        ███░░  3/5  2 contrast failures, no focus rings on cards
Dark Mode            ████░  4/5  Background system solid, one hard-coded color
Mobile Quality       ██░░░  2/5  Nav breaks at 375px, touch targets too small
Brand Distinctiveness ██░░░ 2/5  Generic SaaS pattern — no differentiation

Priority fixes: State Coverage → Hierarchy → Mobile Quality
```

---

## Pro Feature 2 — Figma Token Export

Trigger: *"export tokens"*, *"Figma tokens"*, *"design tokens"*

Generate tokens in W3C Design Token format (compatible with Figma Variables, Style Dictionary, Theo):

```json
{
  "$schema": "https://tr.designtokens.org/format/",
  "color": {
    "base": {
      "background": { "$value": "#0A0A0B", "$type": "color" },
      "subtle": { "$value": "#111113", "$type": "color" },
      "ui": { "$value": "#1A1A1F", "$type": "color" }
    },
    "surface": {
      "default": { "$value": "#222228", "$type": "color" },
      "raised": { "$value": "#2A2A32", "$type": "color" },
      "overlay": { "$value": "#323240", "$type": "color" }
    },
    "accent": {
      "default": { "$value": "#6E56CF", "$type": "color" },
      "hover": { "$value": "#7C66DC", "$type": "color" },
      "active": { "$value": "#6248C0", "$type": "color" }
    },
    "semantic": {
      "success": { "$value": "#30A46C", "$type": "color" },
      "warning": { "$value": "#F76B15", "$type": "color" },
      "error": { "$value": "#E5484D", "$type": "color" },
      "info": { "$value": "#0091FF", "$type": "color" }
    }
  },
  "typography": {
    "scale": {
      "xs": { "$value": "0.75rem", "$type": "dimension" },
      "sm": { "$value": "0.875rem", "$type": "dimension" },
      "base": { "$value": "1rem", "$type": "dimension" },
      "lg": { "$value": "1.125rem", "$type": "dimension" },
      "xl": { "$value": "1.25rem", "$type": "dimension" },
      "2xl": { "$value": "1.5rem", "$type": "dimension" },
      "3xl": { "$value": "1.875rem", "$type": "dimension" },
      "4xl": { "$value": "2.25rem", "$type": "dimension" },
      "5xl": { "$value": "3rem", "$type": "dimension" },
      "6xl": { "$value": "3.75rem", "$type": "dimension" }
    }
  },
  "spacing": {
    "1": { "$value": "4px", "$type": "dimension" },
    "2": { "$value": "8px", "$type": "dimension" },
    "3": { "$value": "12px", "$type": "dimension" },
    "4": { "$value": "16px", "$type": "dimension" },
    "6": { "$value": "24px", "$type": "dimension" },
    "8": { "$value": "32px", "$type": "dimension" },
    "12": { "$value": "48px", "$type": "dimension" },
    "16": { "$value": "64px", "$type": "dimension" },
    "24": { "$value": "96px", "$type": "dimension" },
    "32": { "$value": "128px", "$type": "dimension" }
  },
  "radius": {
    "none": { "$value": "0px", "$type": "dimension" },
    "sm": { "$value": "4px", "$type": "dimension" },
    "md": { "$value": "8px", "$type": "dimension" },
    "lg": { "$value": "12px", "$type": "dimension" },
    "xl": { "$value": "16px", "$type": "dimension" },
    "full": { "$value": "9999px", "$type": "dimension" }
  }
}
```

Also generate the CSS custom properties version and a `tailwind.config.ts` extension block.

---

## Pro Feature 3 — Extended Aesthetics

Beyond the base 8 voices, Pro unlocks:

| Voice | Description | Key Signals |
|---|---|---|
| `neo-brutalist` | Brutalism with color — bold fills, thick borders, offset shadows | Black borders, solid fills, translate shadows |
| `swiss-international` | Grid-obsessed, typography-driven, Helvetica energy | Strict grid, red accents, Helvetica/Neue Haas |
| `y2k-revival` | Early 2000s web — chrome, bevels, gradients, shine | Metallic gradients, pixel fonts, star bursts |
| `vaporwave` | Synthwave palette, grid floors, neon on dark | Magenta + cyan, grid perspective, glow |
| `organic-editorial` | Natural textures, earthy palette, hand-drawn feel | Serif type, grain texture, muted earth tones |
| `corporate-futurism` | Polished enterprise, geometric, confident | Navy + gold, geometric sans, structured grids |
| `soft-ui` (neumorphism) | Extruded surfaces, inset shadows, monochromatic | Same-hue shadows, convex/concave surfaces |
| `terminal-hacker` | Green on black, monospace everything, CRT artifacts | Phosphor green, scanlines, cursor blink |
| `kawaii-tech` | Soft pastel, rounded everything, playful iconography | Pastels, 24px+ radius, blob shapes |
| `luxury-minimal` | Extreme whitespace, thin serifs, gold accents | Lots of air, thin weight type, gold/cream |
| `data-dense` | Bloomberg terminal energy, maximum information | Tight line height, tabular nums, muted palette |
| `sports-energy` | Bold, diagonal, kinetic — ESPN/Nike energy | Diagonal cuts, bold condensed type, electric colors |

---

## Pro Feature 4 — Micro-Interaction Library

Ready-to-use interaction patterns by trigger:

### Button Press
```css
.btn { transition: transform 100ms var(--ease-out), box-shadow 100ms var(--ease-out); }
.btn:active { transform: scale(0.97) translateY(1px); box-shadow: 0 1px 2px rgba(0,0,0,0.3); }
```

### Card Lift
```css
.card { transition: transform 200ms var(--ease-out), box-shadow 200ms var(--ease-out); }
.card:hover { transform: translateY(-4px); box-shadow: 0 12px 32px rgba(0,0,0,0.15); }
```

### Input Focus Expand
```css
.input { transition: border-color 150ms, box-shadow 150ms, padding 150ms; }
.input:focus { padding-left: 14px; box-shadow: 0 0 0 3px rgba(var(--accent), 0.2); }
```

### Checkbox Check Animation
```css
@keyframes check { 0% { stroke-dashoffset: 20; } 100% { stroke-dashoffset: 0; } }
.checkbox-icon { stroke-dasharray: 20; animation: check 200ms var(--ease-out) forwards; }
```

### Skeleton Shimmer
```css
@keyframes shimmer { from { background-position: -200% 0; } to { background-position: 200% 0; } }
.skeleton {
  background: linear-gradient(90deg, var(--surface-default) 25%, var(--surface-raised) 50%, var(--surface-default) 75%);
  background-size: 200% 100%;
  animation: shimmer 1.5s infinite;
}
```

### Toast Slide-In
```css
@keyframes toast-in { from { transform: translateX(calc(100% + 1rem)); opacity: 0; } to { transform: translateX(0); opacity: 1; } }
.toast { animation: toast-in 300ms var(--spring) forwards; }
```

### Number Count-Up (JS)
```js
function countUp(el, target, duration = 1000) {
  const start = performance.now();
  requestAnimationFrame(function tick(now) {
    const progress = Math.min((now - start) / duration, 1);
    const eased = 1 - Math.pow(1 - progress, 3); // ease-out cubic
    el.textContent = Math.round(eased * target).toLocaleString();
    if (progress < 1) requestAnimationFrame(tick);
  });
}
```

---

## Pro Feature 5 — Fluid Type System

Replace fixed type scales with fully fluid clamp-based scales:

```css
:root {
  /* Fluid type: scales between 375px and 1280px viewport */
  --text-xs:   clamp(0.694rem,  0.66rem  + 0.17vw,  0.75rem);
  --text-sm:   clamp(0.833rem,  0.79rem  + 0.22vw,  0.875rem);
  --text-base: clamp(1rem,      0.95rem  + 0.26vw,  1.125rem);
  --text-lg:   clamp(1.2rem,    1.13rem  + 0.35vw,  1.375rem);
  --text-xl:   clamp(1.44rem,   1.34rem  + 0.5vw,   1.75rem);
  --text-2xl:  clamp(1.728rem,  1.59rem  + 0.69vw,  2.25rem);
  --text-3xl:  clamp(2.074rem,  1.89rem  + 0.92vw,  2.75rem);
  --text-4xl:  clamp(2.488rem,  2.24rem  + 1.24vw,  3.5rem);
  --text-5xl:  clamp(2.986rem,  2.65rem  + 1.68vw,  4.5rem);
  --text-6xl:  clamp(3.583rem,  3.14rem  + 2.22vw,  5.5rem);
}
```

Also generate fluid spacing:
```css
:root {
  --space-s:  clamp(0.75rem, 0.70rem + 0.26vw, 1rem);
  --space-m:  clamp(1rem,    0.95rem + 0.26vw, 1.5rem);
  --space-l:  clamp(1.5rem,  1.41rem + 0.43vw, 2rem);
  --space-xl: clamp(2rem,    1.86rem + 0.69vw, 3rem);
  --space-2xl: clamp(3rem,   2.77rem + 1.04vw, 4.5rem);
  --space-3xl: clamp(4rem,   3.68rem + 1.56vw, 6rem);
}
```

---

## Pro Feature 6 — Multi-Page Coherence Check

Trigger: *"check consistency across pages"*, *"review the full app"*

When given multiple components or pages, audit for:

1. **Token drift** — same semantic meaning, different values across pages
2. **Pattern inconsistency** — same UI problem solved differently in different places
3. **Navigation coherence** — active states, breadcrumbs, back patterns consistent
4. **Motion contract** — same interaction, same animation everywhere
5. **Breakpoint alignment** — layout shifts happen at the same breakpoints
6. **Tone drift** — copy voice inconsistent between sections

Output a cross-page diff table showing which elements conflict and which page should be the canonical reference.

---

## Pro Feature 7 — Component Spec Output

Trigger: *"write a spec for this"*, *"document this component"*

Generate a component spec in this format:

```markdown
## ComponentName

**Purpose:** One sentence on what this component does for the user.

**Variants:** list all variant props and their visual effect

**States:** default | hover | focus | active | disabled | loading | error | empty

**Props:**
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| variant | 'primary' \| 'secondary' \| 'ghost' | 'primary' | Visual style |
| size | 'sm' \| 'md' \| 'lg' | 'md' | Height and padding scale |
| loading | boolean | false | Shows spinner, disables interaction |

**Accessibility:**
- Role: button
- Keyboard: Enter / Space to activate
- ARIA: aria-disabled when disabled, aria-busy when loading

**Do:** use for primary actions, one per view section
**Don't:** use more than one primary button per screen area
```
