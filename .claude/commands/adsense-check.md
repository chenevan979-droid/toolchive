# AdSense Optimizer

Review ad placement and compliance across Toolchive pages. Use after AdSense approval.

## Checks

### Compliance
- No more than 3 ad units per page (Google policy)
- Ads are not placed in a way that encourages accidental clicks
- No ads in pop-ups or modals
- Ad containers have clear boundaries (not blending with content deceptively)
- No ads above the fold that push main content down excessively

### Placement Quality
- **Result-adjacent ad**: `.ad-container` exists below the calculator result area
- **Mid-content ad**: ad slot between FAQ items or content sections
- **Sidebar ad**: on desktop layouts wider than 1024px, check for sidebar opportunity
- Ad containers are present but NOT filled with test content (just reserved slots)

### Technical
- AdSense script tag is present in `<head>`: `adsbygoogle.js`
- Each ad slot has correct `data-ad-client` and `data-ad-slot` attributes
- Ad containers are responsive (use `data-ad-format="auto"` or fluid)
- No duplicate ad slot IDs on the same page

### Performance Impact
- AdSense script uses `async` attribute
- No render-blocking ad scripts
- Page still loads and functions with ad blocker enabled (graceful degradation)

## Output

Per-page table:
| Page | Ad Slots | Compliance | Placement Score | Issues |

Summary with recommendations for improving ad revenue without hurting UX.

## Important
- Never add actual ad code or modify ad configurations — only audit and recommend
- The PM (user) makes final decisions on ad placement strategy
