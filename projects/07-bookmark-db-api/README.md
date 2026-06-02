[← Back to projects](../README.md)

# Project 7: Database-Backed Bookmark API

## Goal

Extend Project 6 by replacing the in-memory store with a database-backed store.

Recommended starting point:

- SQLite first for simplicity
- PostgreSQL later for production realism

## Focus Areas

- `database/sql`
- Connection pools
- Migrations
- Transactions
- Context timeout
- SQL error handling
- Repository pattern
- Integration tests

## Completion Criteria

- Database schema is managed by migrations.
- All database operations accept context.
- Include at least one transaction example.
- Provide integration tests.
- Configure the connection pool intentionally.
