# Backend Coding Standards

A single-page, self-contained standards document for writing server-side code.

**Stack covered:** Node.js · Express · SQL via an ORM (Prisma / Sequelize / TypeORM) or
MongoDB via Mongoose

It is **tech-based, not project-based** — apply it to any Node/Express service you work
on. It covers how to split code into layers, what to name things, how to validate input,
how to return data, and what to think about before you call a feature done.

## Read it

| Method | Steps |
| --- | --- |
| Locally | Open [`index.html`](index.html) in a browser — no build step, no dependencies |
| Served | `npx serve .` then visit the printed URL |

The document is a single HTML file with inline CSS, a sticky sidebar for navigation, and
automatic light/dark theming via `prefers-color-scheme`.

## Repository layout

| File | Status |
| --- | --- |
| [`index.html`](index.html) | **Current revision — read this one.** Splits the database chapter into relational/ORM and MongoDB/Mongoose tracks, and organises code by domain. |
| [`nodejs-2.0.html`](nodejs-2.0.html) | Earlier revision, kept for reference. |
| [`nodejs-1.0.html`](nodejs-1.0.html) | First revision, kept for reference. Single combined "Database & ORM" chapter. |

Only `index.html` is maintained. The numbered files exist so teams still following an
older revision can diff against what changed.

## Rule levels

Every rule in the document is tagged with one of three levels:

| Level | Meaning |
| --- | --- |
| **MUST NOT** | Breaks the system or fails code review. No exceptions. |
| **SHOULD** | The expected way. Deviate only with a written reason in the pull request. |
| **TIP** | Helpful, not mandatory. |

When a rule does not fit your case, raise it *before* you deviate. A one-sentence answer
now is cheaper than a rewrite later.

## Contents

1. How to use this document
2. Core principles
3. Architecture
4. Project structure
5. Domain anatomy
6. Layer responsibilities
7. Request lifecycle
8. Naming conventions
9. Case convention boundary
10. Routing rules
11. Validation layer
12. Controller layer
13. Service layer
14. Database — relational & ORMs (14.1), MongoDB & Mongoose (14.2)
15. Middleware
16. Responses & errors
17. Pagination & filtering
18. Auth, permissions and tenancy
19. Configuration & environment variables
20. Logging & audit trail
21. API documentation
22. Background jobs & scheduling
23. Realtime (WebSocket)
24. Security checklist
25. Performance
26. Testing
27. Formatting & imports
28. Building a feature — the order of work
29. Review checklist — common mistakes

## Related standards

| Repository | Scope |
| --- | --- |
| [react-guideline](https://github.com/henrywindson/react-guideline) | Component design, state, hooks, forms, accessibility |
| [nextjs-guideline](https://github.com/henrywindson/nextjs-guideline) | App Router, server vs. client components, caching |

## Contributing

1. Edit [`index.html`](index.html) directly — keep the existing rule-level markup and
   section numbering intact. Do not edit the archived revisions.
2. Adding a section: add both the sidebar link and the section body so navigation stays
   in sync.
3. Open a pull request describing which rule changed and why.
