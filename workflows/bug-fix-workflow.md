# Bug Fix Workflow

## 1. Reproduce the Bug
- Get exact reproduction steps from issue/report
- Verify the bug exists in current codebase
- Note the expected vs actual behavior
- Check if it's environment-specific

## 2. Investigate
```bash
# Check recent changes
git log --oneline -20 -- [affected_files]

# Search for related issues
git log --all --grep="related_keyword"

# Check if tests exist for this behavior
find . -name "*.test.*" | xargs grep -l "related_functionality"
```

## 3. Root Cause Analysis
- Read the failing code path carefully
- Check error logs and stack traces
- Add debug logging if needed
- Form hypothesis about root cause
- Write a test that fails (demonstrating the bug)

## 4. Implement Fix
- Make the minimal change to fix the bug
- Don't refactor surrounding code (separate PR)
- Add/update comments explaining the fix
- Ensure the failing test now passes

## 5. Verify
```bash
# Run the specific test
npm test -- --grep "bug description"

# Run full test suite
npm test

# Check for type errors
npx tsc --noEmit

# Lint
npm run lint
```

## 6. Review Checklist
- [ ] Bug is fixed and test passes
- [ ] No regressions in existing tests
- [ ] Edge cases considered
- [ ] Similar bugs checked in other files
- [ ] Commit message references the issue
