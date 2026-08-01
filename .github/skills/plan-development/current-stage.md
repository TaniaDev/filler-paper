# Current development stage

Last updated: 2026-07-31

## Project purpose

Filler Paper is both:

- a product intended for real use;
- a practical Software Engineering learning project.

The current learning goal is to understand engineering concepts through incremental implementation.

## Technology decisions

### Backend

- Java 21
- Spring Boot 4.1
- Spring Data JPA
- PostgreSQL
- Maven

### Frontend

- Angular 22
- TypeScript 6
- SCSS
- Client-Side Rendering initially
- npm
- Node.js 22 LTS

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

The validated rules are documented in:

```text
../understand-domain/domain.md
```

## Current focus

- configuring GitHub Copilot agent skills;
- preparing the project for incremental feature development.

## Learning context

The following topics have already been introduced at a conceptual level:

- Maven and Maven Wrapper;
- Spring Boot startup and annotations;
- REST controllers;
- MVC and layered architecture;
- initial domain modeling;
- CSR, SSR and SSG;
- CSS, SCSS and Tailwind CSS.

These topics have been introduced but may not yet have been practiced, implemented or mastered.

## Needs repository verification

Before proposing implementation tasks, inspect the repository to confirm:

- which backend modules and classes already exist;
- whether PostgreSQL is configured;
- whether domain entities have been implemented;
- whether the Angular project has been generated successfully;
- which Angular routing and styling options are configured;
- whether frontend and backend communication already exists;
- which tests already exist.

## Planning rule

Prefer one small, testable and understandable learning task at a time.

Do not assume that documentation accurately represents the current implementation.
