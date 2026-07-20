# Page Builder

Generate a new tool/calculator page from the established site template. The user provides the tool name and a brief description of what it calculates.

## Steps

1. **Read an existing page** as the template reference — use `pizza-calculator.html` as the canonical template (it has the latest nav, ad slots, FAQ section, and styling patterns).

2. **Gather from the user** (or infer from the tool name):
   - Tool name (e.g. "Wallpaper Calculator")
   - Primary keyword for SEO
   - What inputs the calculator needs
   - What outputs/results to show
   - 4-6 FAQ questions relevant to the topic

3. **Generate the new HTML file** following these conventions:
   - Filename: kebab-case matching the tool name (e.g. `wallpaper-calculator.html`)
   - Same CSS/styling as template — do NOT create new stylesheets
   - Same nav structure with all existing tool links
   - Same ad slot containers (`.ad-container` divs) in the same positions
   - Same footer with disclaimer link
   - Meta title: "[Tool Name] - Free Online [Tool] | Toolchive"
   - Meta description: 120-155 chars with primary keyword
   - JSON-LD FAQPage schema
   - Calculator logic in inline `<script>` at bottom
   - Mobile-responsive layout matching existing pages

4. **Update navigation** across ALL existing pages — add the new tool to the nav dropdown in every .html file. Use a script or systematic edit to ensure consistency.

5. **Run /seo-check on the new page** to verify SEO compliance.

## Important
- Match the exact visual style, spacing, and color palette of existing pages
- The calculator must actually work — test the math logic
- Include input validation and user-friendly error messages
- Add the new page to sitemap.xml if it exists
