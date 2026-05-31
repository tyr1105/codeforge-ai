# CLAUDE.md - Data Pipeline Project

## Project Overview
[Pipeline name] ingests [data sources] and produces [outputs].

## Tech Stack
- Language: Python 3.12+
- Orchestration: Airflow / Prefect / Dagster
- Processing: Spark / Polars / DuckDB
- Storage: S3 / GCS + BigQuery / Snowflake
- Monitoring: Great Expectations / Soda

## Architecture
- Extract → Transform → Load pattern
- Idempotent operations (safe to re-run)
- Data quality checks at each stage
- Dead letter queue for failed records
- Schema evolution strategy

## Code Style
- Type hints everywhere
- Pydantic for configuration
- DuckDB for local testing
- SQL in dedicated files (not string concat)
- Data catalog for all tables/columns

## Data Quality
- Row count checks
- Schema validation
- Null/empty checks on critical fields
- Freshness checks (data within SLA)
- Cross-source reconciliation

## Testing
- Unit tests for transformations
- Integration tests with sample data
- Contract tests for API sources
- Performance benchmarks for large data
- Data diff for pipeline changes
