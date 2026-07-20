# UI/UX Pro Max

Visual consistency and aesthetic review for Toolchive pages. Accept an optional filename; if omitted, spot-check 5 representative pages.

## Review checklist

### Visual Consistency (cross-page)
- Color palette matches site theme (check CSS variables or inline colors)
- Font sizes and weights are consistent across pages
- Spacing/padding patterns are uniform (input groups, sections, cards)
- Button styles are identical (size, color, border-radius, hover states)
- Ad container positioning is consistent

### Single-page UX
- **Hierarchy**: clear visual flow from inputs → calculate button → results
- **Contrast**: text passes WCAG AA contrast ratio (4.5:1 for body, 3:1 for large)
- **Touch targets**: buttons/inputs at least 44px tall on mobile
- **Loading state**: calculator button has feedback on click
- **Error states**: invalid input shows clear, colored feedback
- **Responsive**: layout works at 375px, 768px, 1280px widths

### Accessibility
- All form inputs have associated `<label>` elements
- Focus order is logical (tab through the page)
- Color is not the only indicator of state (add icons or text too)
- Font size minimum 14px for body text

## How to execute

1. Read the HTML/CSS of each target page
2. Use preview tools to start the dev server and take screenshots at mobile/tablet/desktop
3. Use preview_inspect to verify specific CSS values (colors, spacing, font-size)
4. Report findings as a table: | Page | Issue | Severity | Fix |
5. Offer to auto-fix any issues found
