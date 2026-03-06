# Logo Usage

Rules for using the effectorHQ mark and wordmark across contexts.

---

## The mark

The effectorHQ mark is a stylized claw icon. It represents the core idea: AI that reaches out and acts on the world — an end effector.

**Variants:**

| Variant | File | When to use |
|---------|------|-------------|
| Claw Red on dark | `logos/mark-red-dark.svg` | Dark backgrounds (default) |
| Claw Red on light | `logos/mark-red-light.svg` | Light backgrounds |
| White (knockout) | `logos/mark-white.svg` | Photos, busy backgrounds, overlays |
| Charcoal | `logos/mark-charcoal.svg` | Light backgrounds, monochrome print |

---

## The wordmark

"effectorHQ" as styled text, rendered in Inter SemiBold/Bold. The "HQ" portion is in Claw Red (`#E03E3E`); "effector" is in the primary text color (Bone `#F5F0EB` on dark, Charcoal `#1A1A1A` on light).

| Variant | File | When to use |
|---------|------|-------------|
| Dark mode | `logos/wordmark-dark.svg` | Dark backgrounds |
| Light mode | `logos/wordmark-light.svg` | Light backgrounds |

---

## The lockup

Mark + wordmark together. This is the preferred form for most contexts.

| Variant | File | Orientation |
|---------|------|-------------|
| Horizontal | `logos/lockup-horizontal-dark.svg` | Mark left, wordmark right |
| Stacked | `logos/lockup-stacked-dark.svg` | Mark above, wordmark below |

Use horizontal when width is available. Use stacked for square containers (avatars, favicons at larger sizes).

---

## Clear space

Maintain clear space around the mark equal to the height of the claw's "thumb" — roughly 25% of the mark's total height.

```
          ┌────────────────────┐
          │                    │
          │     ╔══════╗       │
          │     ║ MARK ║       │  ← Clear space = 25% of mark height
          │     ╚══════╝       │     on all sides
          │                    │
          └────────────────────┘
```

For the lockup, clear space is measured from the outermost edges of the combined mark + wordmark.

---

## Minimum size

| Element | Minimum width | Context |
|---------|--------------|---------|
| Mark alone | 24px | Favicons, inline icons |
| Wordmark | 80px | Navigation, headers |
| Lockup (horizontal) | 120px | Headers, footers |
| Lockup (stacked) | 64px | Social avatars |

Below these sizes, use the mark alone — the wordmark becomes illegible.

---

## Color usage rules

1. **Always use Claw Red (`#E03E3E`) for the mark.** No exceptions in digital contexts.
2. On dark backgrounds: red mark, bone/white text.
3. On light backgrounds: red mark, charcoal text.
4. On photos or complex backgrounds: use the white knockout variant.
5. **Never** change the mark color to match a theme or partner brand.

---

## Don'ts

- Don't rotate the mark.
- Don't stretch or distort the proportions.
- Don't add drop shadows, outer glows, or 3D effects.
- Don't place the mark on backgrounds with insufficient contrast (< 3:1 ratio).
- Don't recreate the wordmark in a different font.
- Don't animate the mark in ways that imply aggression or harm (it's a tool, not a weapon).
- Don't lock up the mark with other logos without clear visual separation.

---

## Community usage

If you're building an Effector for OpenClaw, writing a tutorial, or running a community project, you're welcome to use the mark to indicate ecosystem compatibility. Use the standard mark files — don't modify them.

**Suggested patterns:**

```
"Built for the Effector ecosystem" + mark
"Compatible with effectorHQ" + mark
"Powered by effectorHQ" + mark
```

**Don't imply official endorsement:**

```
✗  "Official effectorHQ Partner"     (unless you are)
✗  "Endorsed by effectorHQ"          (unless explicitly)
✗  "effectorHQ Certified"            (no cert program exists yet)
```

---

## File formats

All logo files are provided in:

| Format | Usage |
|--------|-------|
| SVG | Web, documentation, scalable contexts (preferred) |
| PNG @1x | Fallback for contexts that don't support SVG |
| PNG @2x | Retina displays, high-DPI contexts |

SVGs are optimized (SVGO) and use `currentColor` where appropriate for easy theming.

---

## GitHub-specific

For the GitHub organization avatar, use `logos/mark-red-dark.svg` rendered on a `#1A1A1A` background at 500×500px.

For repository social preview images (the card shown when sharing links), use the templates in `templates/social-preview.svg` — fill in the repo name and description.
