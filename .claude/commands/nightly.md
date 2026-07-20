# Nightly Runner

On-demand execution of the full nightly health check suite. Mirrors what the scheduled tasks do, but can be triggered manually at any time.

## Checks

### 1. Site availability
- Fetch `https://toolchive.com` — expect 200
- Fetch 5 random tool pages — expect 200
- Report any pages returning non-200 status

### 2. Content integrity
- Read all HTML files locally
- Check no file is empty or suspiciously small (< 1KB)
- Verify nav section is present in every page
- Verify footer is present in every page

### 3. Git status
- Any uncommitted changes?
- Is local ahead of remote? (unpushed commits)
- Any merge conflicts?

### 4. SEO spot-check
- Pick 3 random pages and run core SEO checks (title, meta desc, H1, schema)
- Report any failures

### 5. Performance baseline
- Count total HTML files and their combined size
- Flag any page over 150KB
- Check for any inline images (base64) that should be external

### 6. Scheduled task status
- List configured scheduled tasks
- Report last run status if available

## Output

```
Nightly Health Check — [date]
━━━━━━━━━━━━━━━━━━━━━━━
✅ Site availability: 6/6 pages OK
✅ Content integrity: 55 pages valid
⚠️ Git: 2 uncommitted files
✅ SEO spot-check: 3/3 passed
✅ Performance: avg 45KB, max 82KB
✅ Scheduled tasks: 4 configured

Overall: HEALTHY (1 warning)
```
