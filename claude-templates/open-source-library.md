# CLAUDE.md - Open Source Library

## Project Overview
[Library name] is a [type] library for [purpose].

## Tech Stack
- Language: TypeScript (ES2022+)
- Build: tsup / unbuild
- Test: Vitest
- Lint: ESLint + Prettier
- Package manager: pnpm

## Code Style
- Functional programming preferred
- No classes unless封装 state
- 100% TypeScript (no JS)
- Comprehensive JSDoc comments
- Export only public API

## API Design
- Small surface area
- Composable functions
- Sensible defaults with override options
- No breaking changes without major version
- Deprecation warnings before removal

## Testing
- 100% type coverage
- 90%+ code coverage
- Property-based tests for utilities
- Edge case testing (null, undefined, empty)
- Cross-platform testing if applicable

## Publishing
- Changesets for versioning
- Conventional commits
- Changelog auto-generated
- CI publishes on release branch merge

## Documentation
- README with quick start
- API reference generated from TSDoc
- Examples in /examples directory
- Migration guides for breaking changes
