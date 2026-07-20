# SEO Checker

Audit one or all tool pages for SEO health. Accept an optional filename argument; if omitted, scan all *.html tool pages (exclude index.html, disclaimer.html).

## Checks to run per page

1. **Title tag**: exists, 50-60 chars, contains primary keyword, no duplicate across site
2. **Meta description**: exists, 120-155 chars, contains keyword, unique
3. **H1**: exactly one, contains keyword
4. **Heading hierarchy**: H1→H2→H3 in order, no skipped levels
5. **Canonical URL**: `<link rel="canonical">` present and correct
6. **Open Graph / Twitter cards**: og:title, og:description, og:image present
7. **Schema.org structured data**: JSON-LD `FAQPage` or `HowTo` present and valid
8. **Image alt text**: all `<img>` tags have descriptive alt attributes
9. **Internal links**: at least 2 internal links to other tool pages
10. **Mobile viewport**: `<meta name="viewport">` present
11. **Page size**: warn if HTML > 100KB
12. **Keyword density**: check the target keyword appears 3-8 times in body text

## Output format

Print a table per page:
| Check | Status | Detail |
Then a summary: X passed, Y warnings, Z failed.

For site-wide scan, also report:
- Duplicate titles or descriptions across pages
- Orphan pages (no internal links pointing to them)
- Missing pages from sitemap.xml (if exists)

## How to run checks

Use the Read tool to read each HTML file. Parse the content to check each rule. Do NOT use external tools or APIs — all checks are local file-based.
