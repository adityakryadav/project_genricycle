# Project Genricycle — DBMS 3rd Semester Project

Structured database-backed application demonstrating end-to-end DBMS concepts: requirements analysis, ER modeling, normalized schema design, SQL implementation, and a minimal application layer to interact with the data.

## Overview

Genricycle encapsulates a complete academic DBMS project:
- Problem definition and scope
- ER diagram and schema design with normalization
- SQL implementation (DDL, DML) with constraints, indexes, and relationships
- Optional stored procedures, triggers, and views
- Sample dataset and queries for evaluation
- Lightweight application interface to showcase CRUD and key workflows

You can tailor the domain focus (e.g., recycling logistics, inventory cycles, generic lifecycle management) using the same schema patterns and queries.

## Features

- Normalized relational schema (3NF or higher where applicable)
- Referential integrity enforced via foreign keys
- Indexing for performance-critical queries
- Sample data seeding for realistic demonstrations
- Representative queries: joins, aggregates, subqueries, and window functions (if supported)
- Optional triggers for audit and consistency
- Optional stored procedures for encapsulated operations

## Tech Stack

- Database: MySQL (or MariaDB)
- SQL assets: DDL (schema), DML (seed), views, triggers, procedures
- Optional app layer: CLI/GUI or simple web frontend to demonstrate usage

Adjust the stack if your implementation uses PostgreSQL, SQLite, or another RDBMS.

## Getting Started

### Prerequisites
- MySQL 5.7+ (or compatible)
- MySQL client (CLI) or GUI (MySQL Workbench/phpMyAdmin)
- Optional: Language runtime for the app layer (e.g., Java/Python/Node)

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/adityakryadav/project_genricycle.git
   cd project_genricycle
   ```
2. Create the database and schema:
   ```sql
   -- Example workflow
   CREATE DATABASE genricycle;
   USE genricycle;
   -- Run DDL scripts provided in the repo (e.g., schema.sql)
   SOURCE path/to/schema.sql;
   ```
3. Seed sample data:
   ```sql
   -- Run DML scripts (e.g., seed.sql)
   SOURCE path/to/seed.sql;
   ```
4. Optional: Set up stored procedures, views, triggers:
   ```sql
   SOURCE path/to/procedures.sql;
   SOURCE path/to/triggers.sql;
   SOURCE path/to/views.sql;
   ```
5. Optional: Run the application layer:
   - Configure DB connection (host, port, user, password, database).
   - Start the app and verify CRUD flows against the DB.

## Database Design

Deliverables typically include:
- Requirements document: entities, relationships, constraints, and key workflows
- ER diagram: entities, cardinalities, participation
- Normalized schema: tables with primary/foreign keys and constraints
- Indexing strategy: clustered/non-clustered indexes and composite keys where suitable
- Integrity and business rules via triggers and constraints

Example entities for a generic lifecycle domain:
- Entity: Item (id, name, category, status)
- Entity: Stage (id, name, sequence)
- Relation: ItemStage (item_id, stage_id, timestamp, notes)
- Supporting tables for users/roles, audits, and catalogs

## Usage

- Run provided queries to demonstrate:
  - Joins across core tables
  - Aggregations and reports
  - Filtering and pagination patterns
  - Integrity checks using constraints and triggers
- Use the app layer (if present) to:
  - Create, read, update, delete items and stages
  - Advance items through lifecycle stages
  - View reports based on joins and aggregates

## Project Structure

Typical layout:
```
project_genricycle/
├─ docs/                # ERD, requirements, normalization steps
├─ sql/                 # schema.sql, seed.sql, views.sql, triggers.sql, procedures.sql
├─ app/                 # optional application layer (CLI/GUI/Web)
├─ README.project_genricycle.md
```

## Evaluation Guide

- Schema correctness: keys, constraints, normalization
- Query coverage: joins, aggregates, subqueries, performance
- Procedural logic: stored procedures/functions (if included)
- Automation: triggers for audit/consistency
- Documentation: ERD, assumptions, and limitations

## Roadmap

- Add comprehensive sample dataset and reports
- Extend triggers for advanced validations
- Implement stored procedures for common operations
- Provide performance notes and indexing benchmarks
- Add unit tests for SQL routines (where feasible)
- Build a minimal web UI to demo workflows

## Contributing

- Fork and create a feature branch
- Keep SQL style consistent (naming, casing, comments)
- Update ERD/docs when schema changes
- Add tests or sample queries for new features
- Open a PR with a clear description and rationale

## License

Specify a license (e.g., MIT). Add a LICENSE file to formalize usage rights.


