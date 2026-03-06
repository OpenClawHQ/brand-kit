# Typography

Type choices for the effectorHQ ecosystem. The system uses two families — one for human language, one for code — and a strict scale.

---

## Font families

### Inter — UI and body text

The workhorse. Inter was designed for computer screens at small sizes. It's neutral, highly legible, and has extensive OpenType features.

```css
font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
```

**Source:** [Google Fonts](https://fonts.google.com/specimen/Inter) / [rsms.me/inter](https://rsms.me/inter)

**Weights used:**

| Weight | Name | Usage |
|--------|------|-------|
| 400 | Regular | Body text, descriptions, long-form content |
| 500 | Medium | UI labels, navigation, subtle emphasis |
| 600 | SemiBold | Subheadings, card titles, section labels |
| 700 | Bold | Page headings, hero text, strong emphasis |

### JetBrains Mono — Code and technical content

Monospaced font for code blocks, terminal output, CLI references, and technical identifiers.

```css
font-family: 'JetBrains Mono', 'Fira Code', 'SF Mono', 'Consolas', monospace;
```

**Source:** [JetBrains](https://www.jetbrains.com/lp/mono/)

**Weights used:**

| Weight | Name | Usage |
|--------|------|-------|
| 400 | Regular | Code blocks, inline code, terminal output |
| 500 | Medium | Emphasized code, filenames, command names |

---

## Type scale

Based on a 1.25 ratio (Major Third) with a 16px base. The scale is intentionally compact — we're building developer tools, not magazines.

| Step | Size | Line height | Usage |
|------|------|-------------|-------|
| `xs` | 12px / 0.75rem | 1.5 | Captions, footnotes, metadata |
| `sm` | 14px / 0.875rem | 1.5 | Secondary text, table content, helper text |
| `base` | 16px / 1rem | 1.6 | Body text, descriptions, form labels |
| `lg` | 20px / 1.25rem | 1.5 | Card titles, section subheadings |
| `xl` | 24px / 1.5rem | 1.4 | Section headings (h3) |
| `2xl` | 32px / 2rem | 1.3 | Page subheadings (h2) |
| `3xl` | 40px / 2.5rem | 1.2 | Page headings (h1) |
| `4xl` | 48px / 3rem | 1.1 | Hero headings, landing pages only |

---

## Pairing rules

### Headings + body

```
h1:   Inter 700, 3xl (40px), Charcoal or Bone
h2:   Inter 600, 2xl (32px)
h3:   Inter 600, xl (24px)
Body: Inter 400, base (16px)
```

### Code in prose

Inline code uses JetBrains Mono at ~90% of the surrounding text size, with a subtle background:

```css
code {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.9em;
  background: rgba(255, 255, 255, 0.06);
  padding: 0.15em 0.35em;
  border-radius: 4px;
}
```

### Technical identifiers

Plugin names, CLI commands, config keys, and file paths always render in JetBrains Mono — even in headings or navigation. This creates a consistent visual language: if it's code-like, it looks code-like.

```
✓  `openclaw init` creates a new project
✗  openclaw init creates a new project
```

---

## Spacing

Text spacing follows an 8px grid. Margins between typographic elements:

| Between | Spacing |
|---------|---------|
| h1 → body | 24px |
| h2 → body | 16px |
| h3 → body | 12px |
| Paragraphs | 16px |
| List items | 8px |
| Code block → text | 24px |

---

## Line length

Optimal reading width: **60–75 characters** per line for body text. On wide screens, constrain the content column — don't let text sprawl.

```css
.prose {
  max-width: 680px;  /* ~65 characters at 16px Inter */
}
```

For code blocks, allow wider lines (up to 100 characters) before horizontal scroll.

---

## Loading fonts

For web projects, load from Google Fonts with `display=swap` to avoid layout shifts:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
```

For README badges and GitHub profiles, fall back to system fonts — GitHub doesn't load custom fonts.
