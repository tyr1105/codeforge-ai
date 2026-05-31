# Python General Cursor Rules

## Code Style
- Python 3.12+ features
- Type hints on ALL function signatures
- Use pathlib over os.path
- f-strings for formatting
- Dataclasses or Pydantic for data containers
- Enums for fixed sets of values

## Patterns
- Protocol for structural typing
- @dataclass(frozen=True) for immutable data
- Generator functions for lazy evaluation
- Context managers for resource management
- Dependency injection via __init__ or function params

## Error Handling
- Custom exception hierarchies
- Use 'raise from' for exception chaining
- Never bare 'except:' (always specify exception type)
- Logging over print statements
- Early return pattern

## Async
- async/await for I/O operations
- asyncio.gather for concurrent tasks
- aiohttp or httpx for async HTTP
- async generators for streaming
- Use anyio for framework-agnostic async

## Testing
- pytest with fixtures
- Parametrize for data-driven tests
- Mock/patch only external dependencies
- Coverage target: 80%+
