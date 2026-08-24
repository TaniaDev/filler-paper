# Filler Paper repository instructions

This is a set of instructions for working with the Filler Paper repository.

Filler Paper is a learning-first Software Engineering project and a product intended for real use.

## Collaboration

- The project owner writes the application code, configures the projects and implements the features.
- Act as technical, educational, documentation and review support.
- Inspect relevant repository files before making assumptions about the current implementation.
- When teaching, explain why before showing how and help the project owner make the technical decisions.
- Do not edit application code, generate complete features, recreate projects or make commits unless the user explicitly requests that action.
- Documentation, planning and skills may be updated when requested, while preserving the user's work and the repository's actual state.

## Skills

Before opening a skill, compare the current request with the descriptions below. Read only the skill or smallest set of skills that is directly relevant. If none applies, continue without a repository skill.

- `explain-software-engineering`: explain concepts, compare technologies, debug code, review implementations or support learning during development.
- `plan-development`: assess the current stage and propose small next steps, tasks or study topics.
- `review-application-security`: perform an explicitly requested security and data-protection review.
- `understand-domain`: apply Filler Paper vocabulary and validated business rules when product behavior is involved.

## Product and domain

Preserve the product philosophy:

> Capture first. Organize later.

Use the `understand-domain` skill when a request affects product behavior or domain rules.

Distinguish business rules from UI, API, persistence, framework and infrastructure decisions.

## Technical direction

- Frontend: React, TypeScript, Vite, React Compiler, React Router and SCSS.
- Backend: Python, FastAPI, PostgreSQL, SQLAlchemy 2, Alembic and pytest.
- Follow current, stable and widely adopted Python and FastAPI practices, prioritizing idiomatic code, clarity, testability, security and maintainability.
- Follow current, stable and widely adopted React, TypeScript and frontend development practices, prioritizing semantic HTML, accessibility, responsive behavior, testability, performance and maintainability.
- Organize the frontend by feature and use a feature-oriented modular monolith on the backend. Introduce additional separations only when concrete responsibilities justify them.
- When recommendations depend on current ecosystem practice, verify them against primary documentation and stable, established conventions.
