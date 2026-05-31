# Python + FastAPI Cursor Rules

## Project Structure
- src/ layout: api/, core/, models/, schemas/, services/
- Use pyproject.toml (no setup.py)
- Dependency injection via Depends()
- Alembic for database migrations

## Code Style
- Python 3.12+ features (type hints, pattern matching, f-strings)
- Pydantic v2 models (model_config, field validators)
- Async by default (async def, await)
- Use dependency injection for DB sessions, auth, config
- Type annotations on ALL functions

## API Design
- RESTful routes in api/ directory
- Router prefix: APIRouter(prefix="/api/v1/users")
- Response models defined in schemas/
- Use HTTPException for errors
- Background tasks for async work

## Database
- SQLAlchemy 2.0 with async engine
- Repository pattern for data access
- Alembic migrations (auto-generate, review before apply)
- Use async sessions: AsyncSession

## Authentication
- JWT tokens via python-jose
- OAuth2 with PasswordBearer
- Role-based access via dependencies
- API key auth for service-to-service

## Testing
- pytest with pytest-asyncio
- TestClient for API tests
- Factory pattern for test data
- Docker compose for integration tests
