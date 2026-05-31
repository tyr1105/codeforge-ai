# Feature Development Workflow

## 1. Planning
- Break feature into small, testable increments
- Define acceptance criteria for each increment
- Identify affected files and modules
- Consider backward compatibility

## 2. Branch Setup
```bash
git checkout main
git pull origin main
git checkout -b feature/[feature-name]
```

## 3. Implementation Order
1. **Types/Interfaces** - Define data structures first
2. **Data Layer** - Repository/service functions
3. **Business Logic** - Core feature logic
4. **API/Controller** - HTTP handlers or RPC endpoints
5. **UI Components** - Frontend components
6. **Integration** - Wire everything together
7. **Tests** - Unit + integration tests

## 4. Testing Strategy
- Write tests alongside code (not after)
- Test happy path first, then edge cases
- Mock external dependencies
- Integration test for critical paths
- Visual regression for UI changes

## 5. Code Quality
```bash
# Type check
npx tsc --noEmit

# Lint
npm run lint

# Format
npm run format

# Test
npm test -- --coverage
```

## 6. PR Preparation
- Squash related commits (keep meaningful history)
- Update documentation
- Add CHANGELOG entry
- Write clear PR description with screenshots
- Self-review before requesting review
