# Ruby on Rails Cursor Rules

## Project Structure
- Standard Rails: app/models, app/controllers, app/views
- Concerns for shared behavior
- Services in app/services/
- Presenters/Decorators with Draper or dry-view
- Use Zeitwerk autoloading

## Code Style
- Ruby 3.2+ features (endless methods, pattern matching)
- Frozen string literals
- Use ActiveModel::Attributes in models
- Service Object pattern for complex operations
- Scope chains for queries

## API Design
- rails-api with JSON:API or Blueprint
- Versioned routes: /api/v1/
- Strong parameters
- Pagination with pagy or kaminari
- Error responses with consistent format

## Database
- PostgreSQL with pgcrypto extensions
- ActiveRecord migrations with change methods
- Use counter caches where appropriate
- Database-level constraints (NOT NULL, FK)
- Concerns for shared model behavior

## Testing
- RSpec with FactoryBot
- System tests with Capybara
- Shoulda Matchers for common validations
- VCR for HTTP stubbing
- CI with parallel_tests

## Background Jobs
- Sidekiq with Redis
- ActiveJob for interface
- Job uniqueness with sidekiq-unique-jobs
- Batch processing for large datasets
