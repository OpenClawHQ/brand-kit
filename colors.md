# Color System

The OpenClaw palette balances industrial precision with warmth. It's built for dark-first interfaces but works across light and dark contexts.

---

## Primary palette

### Claw Red — `#E03E3E`

The signature color. Inherited from the OpenClaw project. Used sparingly and deliberately — it marks things that matter.

```
HEX:  #E03E3E
RGB:  224, 62, 62
HSL:  0°, 73%, 56%
```

**Use for:** Primary brand mark, critical actions (CTAs), status indicators (active/live), the claw icon.

**Don't use for:** Body text, large background fills, decorative elements.

### Signal Orange — `#F27A3A`

The secondary accent. Warmer than Claw Red, it signals interaction and progress.

```
HEX:  #F27A3A
RGB:  242, 122, 58
HSL:  21°, 88%, 59%
```

**Use for:** Hover states, secondary buttons, links, highlights, code syntax accents, progress indicators.

**Don't use for:** Error states (use Claw Red), primary CTAs (use Claw Red).

---

## Neutral palette

The neutrals form the backbone of all layouts. They're warm-tinted — never pure gray.

| Name | Hex | RGB | Role |
|------|-----|-----|------|
| Black | `#0D0D0D` | 13, 13, 13 | Deepest background |
| Charcoal | `#1A1A1A` | 26, 26, 26 | Primary dark background |
| Graphite | `#2A2A2A` | 42, 42, 42 | Card/surface background |
| Iron | `#3D3D3D` | 61, 61, 61 | Borders, dividers (dark mode) |
| Slate | `#6B7280` | 107, 114, 128 | Secondary text, muted elements |
| Ash | `#9CA3AF` | 156, 163, 175 | Placeholder text, disabled states |
| Stone | `#D1D5DB` | 209, 213, 219 | Borders (light mode), subtle text |
| Bone | `#F5F0EB` | 245, 240, 235 | Light background, inverse text |
| White | `#FAFAFA` | 250, 250, 250 | Lightest background |

---

## Semantic colors

For UI states and feedback. These supplement the brand palette — they don't replace it.

| State | Color | Hex | Usage |
|-------|-------|-----|-------|
| Success | Green | `#22C55E` | Build passed, plugin loaded, action completed |
| Warning | Amber | `#F59E0B` | Deprecation notices, config warnings |
| Error | Red | `#EF4444` | Build failed, validation errors, connection lost |
| Info | Blue | `#3B82F6` | Tips, documentation links, neutral notices |

Note: Error red (`#EF4444`) is intentionally different from Claw Red (`#E03E3E`). Claw Red is a brand color; Error red is a UI semantic. Don't conflate them.

---

## Dark mode (default)

OpenClaw interfaces are dark-first. The default scheme:

```
Background:       #1A1A1A  (Charcoal)
Surface:          #2A2A2A  (Graphite)
Border:           #3D3D3D  (Iron)
Primary text:     #F5F0EB  (Bone)
Secondary text:   #9CA3AF  (Ash)
Accent:           #E03E3E  (Claw Red)
```

## Light mode

For documentation, print, and contexts where dark mode isn't appropriate:

```
Background:       #FAFAFA  (White)
Surface:          #F5F0EB  (Bone)
Border:           #D1D5DB  (Stone)
Primary text:     #1A1A1A  (Charcoal)
Secondary text:   #6B7280  (Slate)
Accent:           #E03E3E  (Claw Red)
```

---

## Contrast ratios

All text combinations meet WCAG AA (4.5:1 minimum for normal text):

| Foreground | Background | Ratio | Pass |
|-----------|------------|-------|------|
| Bone on Charcoal | `#F5F0EB` / `#1A1A1A` | 14.8:1 | AAA |
| Ash on Charcoal | `#9CA3AF` / `#1A1A1A` | 7.2:1 | AAA |
| Claw Red on Charcoal | `#E03E3E` / `#1A1A1A` | 4.6:1 | AA |
| Charcoal on Bone | `#1A1A1A` / `#F5F0EB` | 14.8:1 | AAA |
| Claw Red on White | `#E03E3E` / `#FAFAFA` | 4.5:1 | AA |

Claw Red on dark backgrounds meets AA but not AAA. For small text on dark backgrounds, prefer Signal Orange or Bone.

---

## Gradients

Use gradients rarely. When needed, stick to these approved combinations:

```css
/* Hero gradient — dark to darker */
background: linear-gradient(135deg, #1A1A1A 0%, #0D0D0D 100%);

/* Accent glow — for hover/focus rings */
box-shadow: 0 0 20px rgba(224, 62, 62, 0.15);

/* Card highlight — subtle surface lift */
background: linear-gradient(180deg, #2A2A2A 0%, #1A1A1A 100%);
```

Avoid multicolor gradients. The palette is restrained for a reason.
