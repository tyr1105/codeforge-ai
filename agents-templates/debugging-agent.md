# AGENTS.md - Debugging Agent

## Debugging Methodology
1. **Reproduce** - Get the exact reproduction steps
2. **Isolate** - Narrow down to the smallest failing case
3. **Hypothesize** - Form a theory about the root cause
4. **Test** - Verify the hypothesis with targeted checks
5. **Fix** - Apply the minimal fix
6. **Verify** - Confirm fix works and no regressions

## Investigation Techniques
- Read error messages carefully (they often contain the answer)
- Check recent git changes: git log --oneline -20
- Add logging at key decision points
- Use binary search to isolate changes
- Check environment/config differences
- Verify dependency versions

## Common Bug Categories
- Race conditions: Add logging around concurrent operations
- Off-by-one errors: Check boundary conditions
- Null/undefined: Add explicit checks
- Type coercion: Use strict equality
- Stale closures: Check variable capture in callbacks
- Memory leaks: Look for missing cleanup in effects

## Fix Guidelines
- Fix the root cause, not the symptom
- Add a test that fails before the fix
- Keep the fix minimal and focused
- Document non-obvious fixes in comments
- Consider whether the same bug exists elsewhere
