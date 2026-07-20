# Webapp Testing

Comprehensive functional testing for Toolchive calculator pages. Goes beyond /verify by testing calculator logic, edge cases, and cross-page consistency.

## Usage

Accept an optional filename; if omitted, test all calculator pages.

## Test suite per page

### 1. Page loads correctly
- Start dev server with preview_start if not running
- Navigate to the page
- Confirm no console errors (preview_console_logs)
- Confirm no failed network requests (preview_network filter:failed)
- Take a screenshot for visual baseline

### 2. Calculator functionality
- Identify all input fields via preview_snapshot
- Fill inputs with **valid typical values** and click Calculate
- Verify result appears and contains a number (not NaN, not empty)
- Take screenshot of results

### 3. Edge cases
- **Empty inputs**: click Calculate with no values — should show validation error, not crash
- **Zero values**: enter 0 in numeric fields — should handle gracefully
- **Negative numbers**: enter -1 — should reject or handle appropriately
- **Very large numbers**: enter 999999999 — should not overflow or freeze
- **Decimal inputs**: enter 3.5 where applicable — should work

### 4. Responsive layout
- Test at mobile (375px) — preview_resize preset:mobile
- Test at tablet (768px) — preview_resize preset:tablet
- Verify no horizontal overflow, buttons are tappable, results are readable
- Screenshot each breakpoint

### 5. Cross-page consistency
- Nav links work (click a random nav link, verify it navigates)
- Footer links work
- Back button returns to previous page

## Output

```
Page: pizza-calculator.html
✅ Page load — no errors
✅ Calculator — result: "You need 5 large pizzas"
✅ Empty input — shows "Please fill in all fields"
⚠️ Negative number — accepted -5 guests (should reject)
✅ Mobile layout — no overflow
✅ Nav links — working

Result: 5/6 passed, 1 warning
```
