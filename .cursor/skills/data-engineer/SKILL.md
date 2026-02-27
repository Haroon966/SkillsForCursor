---
name: data-engineer
description: SQL, data analysis, and data scripts. Use when the user works on or asks about data analysis, SQL queries, tables and datasets, local databases (SQLite, local Postgres/MySQL), online/cloud databases, ETL scripts, data pipelines, reporting, aggregations, data profiling, or analyzing data with Python/SQL.
---

# Data Engineer

Apply when working with **data**: writing SQL, analyzing tables, connecting to local or online databases, or creating scripts for ETL, reporting, or data profiling. For application schema design and migrations, see [database-dev](.cursor/skills/database-dev/SKILL.md).

## When to Use This Skill

- Data analysis and exploratory queries
- SQL: SELECT, aggregations, JOINs, window functions
- Tables and datasets (local or remote)
- Local DBs (e.g. SQLite, local Postgres/MySQL)
- Online/cloud databases and connection config
- ETL scripts (extract, transform, load)
- Reporting and aggregations
- Data profiling (counts, nulls, distributions)

## Principles

- **Parameterized queries**: Always use parameters for user or external input; never concatenate into SQL.
- **Destructive ops**: Avoid destructive operations (DELETE, DROP, TRUNCATE) without explicit confirmation or safeguards.
- **Documentation**: Document data sources, assumptions, and script inputs/outputs.
- **Reproducibility**: Prefer scripts (e.g. Python + SQL or runnable SQL) with clear inputs and outputs so runs are reproducible.

## Patterns

- **Connections**: Use connection strings and env vars for credentials; separate config for local vs remote DBs.
- **Analysis**: SELECT and aggregations (GROUP BY, COUNT, SUM, AVG); use window functions when needed for rankings or running totals.
- **Scripts**: Python with sqlite3, psycopg2, or pandas for heavier analysis; keep scripts runnable and idempotent where possible.
- **ETL**: Read from source → transform (filter, aggregate, reshape) → write to target; log row counts or key metrics.
- **Profiling**: Row counts, null counts, value distributions, basic stats to understand data quality and shape.

## Conventions

- Use the project’s preferred language (e.g. Python) and DB drivers.
- Store secrets in env vars or a secrets manager, not in code.
- For schema design and application migrations, see [database-dev](.cursor/skills/database-dev/SKILL.md).
