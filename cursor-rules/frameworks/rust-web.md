# Rust + Axum/Actix Cursor Rules

## Project Structure
- Cargo workspace for multi-crate projects
- src/bin/ for executables, src/lib.rs for library
- Modular: handlers/, models/, services/, middleware/
- Configuration via .env + config crate

## Code Style
- Prefer Result<T, E> with custom error types
- Use thiserror for error definitions, anyhow for apps
- Lifetimes: use owned types when possible, borrow when needed
- Implement traits for domain behavior
- Use tower middleware layers

## Web Framework
- Axum preferred (tower ecosystem)
- State via Arc<AppState> or Extension
- Extractors for request parsing
- JSON responses with serde_json
- WebSocket support via tokio-tungstenite

## Database
- SQLx for async database access
- Compile-time query checking
- Migrations via sqlx-cli
- Use sea-orm for complex queries

## Error Handling
- Custom error enum with thiserror
- IntoResponse implementation for HTTP errors
- Error middleware for logging
- Never panic in production code

## Testing
- Built-in #[test] attributes
- tokio::test for async tests
- Integration tests in tests/
- Property-based testing with proptest
