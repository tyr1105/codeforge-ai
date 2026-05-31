# Rust General Cursor Rules

## Ownership & Borrowing
- Prefer owned types in function returns
- Borrow in function parameters when caller keeps ownership
- Use Arc<Mutex<T>> only when truly needed
- Cow<str> for string flexibility
- Avoid .clone() unless necessary (document why)

## Error Handling
- Result<T, E> everywhere
- thiserror for library errors, anyhow for applications
- ? operator for propagation
- Never unwrap() in production code
- Map_err for error transformation

## Concurrency
- tokio for async runtime
- channels (mpsc, broadcast) for message passing
- rayon for CPU parallelism
- Arc for shared ownership across threads
- Atomic types for lock-free counters

## Performance
- Prefer iterators over loops
- Use &str over String when borrowing
- Pre-allocate Vec with with_capacity
- Zero-copy parsing with nom or winnow
- Profile before optimizing

## Idioms
- Builder pattern with Option fields
- Newtype pattern for domain types
- Trait objects vs generics: profile if uncertain
- derive macros: Debug, Clone, PartialEq at minimum
- Feature flags for optional functionality
