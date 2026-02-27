---
name: database-dev
description: Schema design and migrations for application databases. Use when the user works on or asks about schema design, SQL, migrations, queries, indexes, normalization, data modeling, ORM usage, or database performance.
---

# Database Dev

Apply when designing or changing **application database** schema: models, migrations, indexes, and query performance. For data analysis, ETL, or reporting scripts, see [data-engineer](.cursor/skills/data-engineer/SKILL.md).

## When to Use This Skill

- Schema design: tables, columns, relationships
- Migrations (creating, altering, rolling back)
- Indexes and query performance
- Data modeling and normalization
- ORM usage (e.g. Django ORM) for app data access
- Avoiding N+1 and writing efficient queries

## Principles

- **Migrations**: Prefer reversible migrations; avoid destructive changes (drops, big alters) without backup or a clear safety path.
- **Transactions**: Use transactions for multi-step writes; keep them short.
- **Safety**: No raw DDL in production without review; test migrations on a copy of data when possible.

## Patterns

- **Naming**: Consistent table and column names (snake_case typical); clear, descriptive names for indexes.
- **Indexes**: Add indexes for columns used in WHERE, JOIN, ORDER BY; avoid over-indexing; consider composite indexes for common query patterns.
- **N+1**: Use select_related / prefetch_related (Django) or equivalent to batch-load relations; profile before optimizing.
- **Migration workflow**: One logical change per migration; run migrations in order; have a rollback or forward-only strategy documented.

## Conventions

- In Django projects: use Django migrations and the Django ORM; prefer parameterized queries for raw SQL; document schema changes.
- Align with [backend-dev](.cursor/skills/backend-dev/SKILL.md) (Django) when in the same project (e.g. model placement, migration hygiene).

**Distinction from data-engineer**: This skill focuses on schema and migrations for the application’s database. The data-engineer skill focuses on SQL, data scripts, and analysis (local/remote DBs, ETL, reporting).
