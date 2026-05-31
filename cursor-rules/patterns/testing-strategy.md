# Testing Strategy Cursor Rules

## Test Pyramid
- 70% Unit tests (fast, isolated, many)
- 20% Integration tests (database, API, external)
- 10% E2E tests (user workflows, critical paths)

## Unit Testing
- Test behavior, not implementation
- One assertion per test (or logical group)
- Arrange-Act-Assert pattern
- Mock external dependencies only
- Test naming: should_[expected]_when_[condition]

## Integration Testing
- Use real database (Docker or test containers)
- Test API contracts end-to-end
- Validate request/response schemas
- Test error paths
- Clean up test data between tests

## E2E Testing
- Test critical user journeys
- Use page object model
- Visual regression testing for key pages
- Performance budgets in E2E
- Cross-browser testing for public apps

## CI Integration
- Run unit tests on every commit
- Integration tests on PR
- E2E tests before merge
- Coverage reports as PR comments
- Fail builds on coverage regression
