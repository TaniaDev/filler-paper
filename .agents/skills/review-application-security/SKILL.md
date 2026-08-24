---
name: review-application-security
description: Reviews Filler Paper features involving authentication, authorization, browser storage, user content, Markdown, import, export or sensitive data handling.
---

# Review application security

Review the requested feature from an application security and data-protection perspective.

## Review process

When reviewing a security-sensitive feature:

1. Identify which data enters, leaves or is stored.
2. Identify the trust boundaries involved.
3. Treat user-created content, imported files and browser storage as untrusted.
4. Distinguish authentication from authorization.
5. Verify that authorization is enforced by the backend.
6. Check whether secrets, credentials or sensitive data are stored unsafely.
7. Review Markdown and HTML rendering for script injection risks.
8. Consider confidentiality, integrity and availability.
9. Recommend the smallest effective protection for the current project stage.
10. Separate required protections from future hardening.

Do not describe any feature or implementation as completely secure.

When security depends on an assumption, state that assumption explicitly.

## Security and data handling direction

Security must be considered in both delivery modes from the beginning.

### Public demo mode

- is intended only for temporary, non-sensitive content;
- stores demo content locally in the browser using `localStorage`;
- must not store passwords, tokens or session identifiers in `localStorage`;
- treats all browser-stored and imported data as untrusted;
- must clearly warn users not to enter sensitive or important information;
- does not guarantee durability, confidentiality or synchronization;
- does not send user-created content to the backend;
- should run on an origin separate from the full application.

### Full application mode

- requires authentication and server-side authorization;
- isolates each user's Binders, Dividers, Pages and Tags;
- validates ownership on every protected backend request;
- must not expose credentials or private configuration;
- should use HTTPS and secure session handling;
- should not store authentication credentials in `localStorage`.

### Shared principles

Both modes must:

- treat user-created content as untrusted;
- render Markdown safely;
- avoid executing user-provided HTML or JavaScript;
- validate data at trust boundaries;
- never rely on frontend validation or visibility rules as an authorization boundary;
- fail safely when data is malformed or access is denied.

### Markdown export

Both delivery modes should allow users to export their notes as Markdown files.

Markdown export must:

- be explicitly initiated by the user;
- export only content the user is allowed to access;
- generate safe filenames;
- avoid including credentials, internal identifiers or private application metadata;
- treat exported content as plain text rather than executable HTML;
- preserve the user's original Markdown content whenever safely possible.
