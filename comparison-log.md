# Reset and Token Comparison Log

**Project:** Practice Reset and Token Comparison
**Date:** 2026-08-30

---

## Part A — Reset Comparison

### reset-none.css (Browser Defaults)

**5 Useful Defaults:**
1. Headings keep their size hierarchy (`<h1>` bigger than `<h2>`)
2. Paragraphs and headings have margins
3. Lists have indentation and bullets
4. Links are underlined
5. Buttons/inputs have visible borders and padding

**2 Conflicting Defaults:**
1. Body has an 8px default margin
2. Browser-specific fonts (inconsistent with the design font stack)

### reset-broad.css (Defaults Removed That Must Be Rebuilt)

1. Heading size hierarchy
2. Margins
3. Form control borders

### reset-selective.css (Removals with Justification)

1. Body default margin — allows header to sit edge-to-edge
2. Default form fonts — matches design font stack
3. Inconsistent box sizing — applies `box-sizing: border-box` for predictable layout

### Key Finding

All three resets produced nearly identical visuals because `component-styles.css` loads after and overrides most reset rules. The reset choice matters most for unstyled edge cases (spacing rhythm, heading hierarchy, form boundaries).

---

## Part B — Tokens & Alternate Theme

1. Tokens defined in `:root` (action, accent, surface, text, page, space, radius)
2. All component rules consume tokens via `var(--...)`
3. `.theme-alt` overrides semantic tokens ONLY
4. Alternate theme card: navy button + amber accent + pale blue background
5. Default theme card: maroon + gold + white — clearly different
6. Verification: theme change required editing ONLY token values, zero component rule changes

## Screenshots

-
- reset-none content: ![content](screenshots/beforepart1reset_none.png)
- reset-none actions: ![actions](screenshots/beforepart2reset_none.png)
- reset-broad content: ![content](screenshots/afterpart1reset-borad.png)
- reset-broad actions: ![actions](screenshots/afterpart2reset-borad.png)
- reset-selective content: ![content](screenshots/afterpart1rese-selective.png)
- reset-selective actions: ![actions](screenshots/afterpart2reset-selective.png)
- Part B tokens + theme-alt: ![tokens](screenshots/aftercsschange.png)