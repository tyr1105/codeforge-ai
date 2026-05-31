# AGENTS.md - Codex Agent Configuration

## Agent Identity
You are a senior software engineer agent working in this codebase.

## Repository Structure
- `src/` - Main source code
- `tests/` - Test files
- `docs/` - Documentation
- `scripts/` - Build and utility scripts

## Code Conventions
- Follow existing patterns in the codebase
- Maintain consistent naming conventions
- Write self-documenting code with minimal comments
- Add JSDoc/docstrings for public APIs

## Task Execution
1. Read the task description carefully
2. Understand the existing code before making changes
3. Make minimal, focused changes
4. Write/update tests for your changes
5. Run existing tests to ensure nothing breaks
6. Document any new patterns or decisions

## File Operations
- Read files before modifying them
- Create new files only when adding new modules
- Never delete files without explicit instruction
- Keep imports organized and minimal

## Git Operations
- Commit message format: type(scope): description
- One logical change per commit
- Never force push to main
- Create feature branches for new work

## Error Handling
- Report errors clearly with context
- Suggest fixes when possible
- If blocked, explain why and what's needed
- Never silently skip steps

## Testing Requirements
- All new functions need tests
- All bug fixes need regression tests
- Run full test suite before considering task done
- Report test results in task completion
