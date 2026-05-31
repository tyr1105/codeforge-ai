# Code Review Checklist

## Before You Start
- [ ] Read the PR description completely
- [ ] Understand the context and motivation
- [ ] Check related issues/discussions

## Code Correctness
- [ ] Logic is correct for all cases
- [ ] Edge cases are handled
- [ ] Error handling is comprehensive
- [ ] No race conditions
- [ ] Resource cleanup (memory, connections, files)

## Security Review
- [ ] Input validation present
- [ ] Output encoding applied
- [ ] Authentication verified
- [ ] Authorization checked
- [ ] SQL parameterized (no injection)
- [ ] No sensitive data exposure

## Performance
- [ ] No N+1 queries
- [ ] Appropriate data structures
- [ ] Caching where beneficial
- [ ] No unnecessary DOM operations
- [ ] Efficient algorithms chosen

## Code Style
- [ ] Follows project conventions
- [ ] Descriptive naming
- [ ] Appropriate comments (why, not what)
- [ ] No magic numbers/strings
- [ ] Consistent formatting

## Testing
- [ ] Tests cover new code
- [ ] Tests are meaningful
- [ ] Test naming is descriptive
- [ ] Mocks are appropriate
- [ ] Edge cases tested

## Documentation
- [ ] Public APIs documented
- [ ] Complex logic explained
- [ ] README updated if needed
- [ ] Breaking changes flagged
