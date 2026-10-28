# Tradebook

Tradebook is a FastAPI backend for tracking investment portfolios, accounts, and trades. It brings transaction history, portfolio positions, and transfers between accounts into a single API.

## Status

The project is in its initial stage. The scope below describes planned functionality.

## Planned features

- User registration, authentication, and access to personal accounts.
- Account management and portfolio position tracking.
- Creating, viewing, updating, and deleting trades.
- Trade history with cursor-based pagination.
- Transfers between accounts with transactional balance updates.
- Reports on trading activity by account, instrument, and date.
- Cached market quotes and background report generation.

## Technology

- **API:** Python, FastAPI, Pydantic.
- **Database:** PostgreSQL, SQLAlchemy, Alembic migrations.
- **Authentication:** JWT access and refresh tokens, password hashing.
- **Caching:** Redis.
- **Background jobs:** Celery or an equivalent task queue.
- **Testing:** pytest, HTTP API and database integration tests.
- **Infrastructure:** Docker and Docker Compose.

## Design

The API will separate HTTP routing, business logic, and database access into router, service, and repository layers. Core entities include users, accounts, trades, positions, and transfers.

Account transfers will run within a single database transaction. Access checks will restrict each user's operations to their own data, and trade history will use a stable cursor based on creation time and ID.

## Running locally

Application code and dependency configuration have not been added yet. Setup, migration, and launch instructions will be documented as the implementation becomes available.
