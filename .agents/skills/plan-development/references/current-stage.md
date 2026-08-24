# Current development stage

Last updated: 2026-08-24

## Project purpose

Filler Paper is both:

- a product intended for real use;
- a practical Software Engineering learning project.

The current learning goal is to understand engineering concepts through incremental implementation.

## Technology decisions

### Backend

- Python
- FastAPI
- PostgreSQL
- SQLAlchemy 2
- Alembic
- pytest

### Frontend

- React
- TypeScript
- Vite
- React Compiler
- React Router
- SCSS

C# is studied separately in game projects.

## Product decisions

The core philosophy is:

> Capture first. Organize later.

The main domain concepts are:

- Binder;
- Divider;
- Page;
- Draft;
- Refined;
- Tag;
- Trash.

The validated rules are documented in [the domain reference](../../understand-domain/references/domain.md).

## Current stage

The project is being started again from its initial foundations.

No application feature, architectural layer, persistence integration or test suite should be treated as implemented until it is verified in the repository.

## Current focus

- establishing and verifying the initial frontend and backend projects;
- preparing the repository for incremental feature development;
- keeping documentation aligned with the code that actually exists.

## Delivery strategy

The repository should support two complementary delivery modes:

1. Public demo mode
   - provides a frontend-only React experience;
   - stores demo data locally in the browser using `localStorage`;
   - does not require authentication;
   - does not send user-created content to the backend;
   - is intended for public showcase and low-friction evaluation.

2. Full application mode
   - connects the React frontend to the FastAPI backend API;
   - persists data in PostgreSQL;
   - uses authentication and user data isolation;
   - supports private, invite-only and self-hosted deployments.

Both delivery modes should allow users to export their notes as Markdown files.

Both modes should share the same product behavior, domain rules and user interface whenever possible. They should differ mainly in their persistence and infrastructure integrations.

The demo mode is not a replacement or shortcut for the full application. It provides a simple way to explore the product while the backend-backed application continues to evolve.

## Learning context

The project is restarting from its foundations. Previous implementation work must not be treated as current experience or completed practice without confirmation.

The current learning priorities are:

- Object-Oriented Programming and SOLID;
- domain modeling, encapsulation and invariants;
- software architecture and separation of responsibilities;
- persistence, transactions and PostgreSQL;
- testing and APIs;
- security and professional development practices;
- Python and FastAPI on the backend;
- TypeScript and React on the frontend.

These are learning goals, not evidence that a topic has already been implemented or mastered.

## Needs repository verification

Before proposing implementation tasks, inspect the repository to confirm:

- whether the frontend and backend projects have been initialized successfully;
- which generated scripts, dependencies and configuration actually exist;
- whether PostgreSQL or SQLAlchemy is configured;
- whether domain entities have been implemented;
- which React routing and styling options are configured;
- whether frontend and backend communication exists;
- which tests already exist.

## Planning rule

Prefer one small, testable and understandable learning task at a time.

Do not assume that documentation accurately represents the current implementation.
