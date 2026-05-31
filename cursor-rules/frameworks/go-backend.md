# Go Backend Cursor Rules

## Project Structure
- Standard Go layout: cmd/, internal/, pkg/, api/
- One package per domain concept
- main.go in cmd/server/
- Use go mod for dependency management

## Code Style
- Interface satisfaction: accept interfaces, return structs
- Error wrapping with fmt.Errorf("...: %w", err)
- Context as first parameter in all functions
- Use slices and maps from Go 1.21+
- Table-driven tests

## API Design
- Chi or Gin router
- Middleware chain pattern
- Request/Response structs with JSON tags
- Validator for input validation
- OpenAPI/Swagger docs

## Database
- pgx for PostgreSQL
- sqlc for type-safe queries
- Migrations with golang-migrate
- Transaction pattern with context

## Concurrency
- Goroutines with errgroup for parallel work
- Channels for communication
- sync.Mutex for shared state
- Context cancellation for timeouts

## Testing
- Table-driven tests as standard
- httptest for HTTP handler tests
- Build tags for integration tests
- Testify for assertions
