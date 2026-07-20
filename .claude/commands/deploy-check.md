# Deploy Checker

Verify that a Vercel deployment succeeded after pushing to GitHub.

## Steps

1. **Check git status**: confirm the local branch is pushed and up to date with remote.

2. **Identify what changed**: run `git diff HEAD~1 --name-only` to list changed files.

3. **Wait for deploy**: Vercel deploys typically take 30-90 seconds. Wait ~60 seconds after push.

4. **Verify live site** using WebFetch:
   - Fetch `https://toolchive.com` — confirm 200 status
   - For each changed HTML file, fetch its URL (e.g. `https://toolchive.com/pizza-calculator.html`)
   - Confirm pages return 200, not 404

5. **Content verification**:
   - Check that the fetched page content includes expected changes (new title, new section, etc.)
   - Verify no broken links on changed pages by checking internal href targets

6. **Report**:
   ```
   Deploy Status: SUCCESS / PARTIAL / FAILED
   
   Pages checked:
   ✅ /pizza-calculator.html — 200 OK, content verified
   ❌ /new-tool.html — 404 Not Found
   
   Action needed: [if any]
   ```

## When to use
- After `git push` to main
- After Vercel redeploy
- As part of /schedule daily health check
