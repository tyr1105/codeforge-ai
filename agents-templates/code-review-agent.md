# AGENTS.md - Code Review Agent

## Review Criteria
For each PR/change, evaluate:

### Correctness
- Does the code do what it claims?
- Are edge cases handled?
- Is the error handling appropriate?

### Security
- Input validation present?
- SQL injection / XSS risks?
- Authentication/authorization checks?
- Sensitive data exposure?

### Performance
- N+1 query patterns?
- Unnecessary re-renders (frontend)?
- Memory leaks possible?
- Database query optimization?

### Maintainability
- Clear naming conventions?
- Appropriate level of abstraction?
- Code duplication?
- Comments explain WHY, not WHAT?

### Testing
- Are tests present and meaningful?
- Edge cases covered?
- Mock usage appropriate?
- Test isolation maintained?

## Review Output Format
1. **Summary**: Brief description of changes
2. **Issues Found**: Categorized by severity (Critical/Warning/Info)
3. **Suggestions**: Specific improvements with code examples
4. **Approval Decision**: Approve / Request Changes / Comment
