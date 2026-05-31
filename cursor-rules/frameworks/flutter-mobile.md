# Flutter/Dart Cursor Rules

## Project Structure
- Feature-first: lib/features/[feature]/
- Core: lib/core/ (theme, utils, networking)
- Clean Architecture: data/, domain/, presentation/
- Use melos for multi-package projects

## Code Style
- Dart 3 patterns (records, patterns, sealed classes)
- Freezed for immutable models
- Riverpod for state management
- Use const constructors where possible
- Named parameters with required keyword

## Widget Patterns
- Stateless for pure UI
- ConsumerWidget for Riverpod
- Widget composition over inheritance
- Extract reusable widgets
- Use Builder pattern for complex widgets

## State Management
- Riverpod 2.0 with code generation
- AsyncValue for loading/error states
- StateNotifier for complex state
- Use ref.watch in build, ref.read in callbacks

## API & Data
- dio for HTTP client
- Retrofit for API clients
- Hive or Isar for local storage
- go_router for navigation
- JSON serialization with json_serializable

## Testing
- Unit tests for business logic
- Widget tests for UI
- Integration tests with patrol
- Golden tests for pixel-perfect UI
