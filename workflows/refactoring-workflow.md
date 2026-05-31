# Refactoring Workflow

## Safety Rules
- Refactor ONE thing at a time
- Run tests after each change
- Keep commits small and atomic
- Don't mix refactoring with feature work

## Step-by-Step Process

### 1. Preparation
- Ensure all tests pass before starting
- Add characterization tests if coverage is low
- Identify the scope of changes
- Create a feature branch

### 2. Small Steps
```
For each refactoring:
1. Make the change
2. Run tests
3. Commit if green
4. Repeat
```

### 3. Common Refactoring Patterns
- **Extract Function**: Long method → smaller functions
- **Rename**: Unclear names → descriptive names
- **Move**: Misplaced code → correct module
- **Replace Conditional**: if/switch → polymorphism
- **Introduce Parameter Object**: Many params → single object
- **Simplify Conditional**: Nested ifs → guard clauses

### 4. Verification
```bash
# Full test suite
npm test

# Type checking
npx tsc --noEmit

# Lint
npm run lint

# Check for behavioral changes
git diff --stat
```

### 5. Cleanup
- Remove any TODO comments you created
- Verify no unused imports remain
- Check bundle size impact (frontend)
- Update documentation if public API changed
