---
name: understand-domain
description: Provides the product philosophy, vocabulary, and domain rules of Filler Paper. Use when designing or reviewing binders, dividers, pages, organization, refinement status, use cases, APIs, persistence, or product behavior.
---

# Filler Paper domain guidance

Consult the relevant sections of [references/domain.md](references/domain.md) before proposing changes that affect product behavior or domain rules.

When working with the domain:

1. Identify the concepts and business rules affected by the request.
2. Preserve the philosophy "Capture first. Organize later."
3. Distinguish business rules from UI, API, persistence and framework decisions.
4. Use the vocabulary defined in [references/domain.md](references/domain.md).
5. Preserve the documented domain invariants.
6. Explain the consequences and trade-offs of changing a rule.
7. Do not invent missing business rules.
8. Clearly identify decisions that have not been defined yet.

When proposing domain APIs, prefer intention-revealing operations such as:

- `page.moveTo(divider)`
- `page.markAsRefined()`
- `binder.addPage(page)`

Avoid representing every domain operation only through public setters.
