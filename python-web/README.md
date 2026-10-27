# Python Web & Backend Engineering — Full Track Record

**vrboddhula** · [← Back to profile](../README.md) · Updated 2026-10-27

## Progress

[░░░░░░░░░░░░░░░░░░░░] 0%   (0 of 45 projects completed)

## Web & HTTP Foundations

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Make your backend an HTTP client: call third-party APIs with httpx (sync and async), handle timeouts, retries, and errors, and keep API keys server-side. | ⬜ Not started | — | — | — |
| Add interactivity to server-rendered pages using HTMX — swap HTML fragments returned by your backend on user actions, no JavaScript framework required. | ⬜ Not started | — | — | — |
| Build a small Flask web app with routes, request handling, and JSON responses — your first real (WSGI) web framework after the no-framework server. | ⬜ Not started | ⚠️ Unverified | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-python-web/issues/2) |
| Build a FastAPI app with type-hinted path operations, automatic validation, and auto-generated interactive docs — the modern async Python API framework. | ⬜ Not started | ⚠️ Unverified | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-python-web/issues/3) |
| Render HTML pages from templates with Jinja2: template inheritance, passing data, loops/conditionals, and why autoescaping protects against XSS. | ⬜ Not started | — | — | — |
| Build a tiny HTTP server with no web framework to learn methods, status codes, headers, and the request/response cycle — plus WSGI vs ASGI. | ⬜ Not started | ⚠️ Unverified | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-python-web/issues/1) |
| Master FastAPI's parameter system — path, query, and body params with validation constraints — and response_model for shaping and filtering output. | ⬜ Not started | — | — | — |

## REST APIs & Validation

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Add scalable list endpoints: offset and cursor pagination, safe filtering and sorting, and metadata so clients can page through large datasets without dumping the whole table. | ⬜ Not started | — | — | — |
| Design and build a clean CRUD REST API for a resource: correct HTTP verbs and status codes, consistent resource URLs, and predictable behavior. | ⬜ Not started | — | — | — |
| Give your API one consistent error shape with custom exceptions and FastAPI exception handlers, so clients always get predictable, useful errors without leaking internals. | ⬜ Not started | — | — | — |
| Accept file uploads safely in FastAPI: enforce type and size limits, store files, serve them back, and reject dangerous or oversized files. | ⬜ Not started | — | — | — |
| Polish your API's auto-generated OpenAPI docs: tags, summaries, descriptions, examples, response documentation, and metadata — so the interactive docs are genuinely useful. | ⬜ Not started | — | — | — |
| Evolve an API without breaking existing clients: URL vs header versioning, organizing versioned routers, and a deprecation strategy. | ⬜ Not started | — | — | — |
| Go beyond basic types: field constraints, custom validators, nested models, computed fields, and clear validation errors — making your API reject bad data at the edge. | ⬜ Not started | — | — | — |
| Use FastAPI's Depends to share logic across endpoints — DB sessions, current-user lookup, pagination params, config — keeping handlers clean and testable. | ⬜ Not started | — | — | — |

## Databases & ORMs

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Map Python classes to database tables with the SQLAlchemy ORM: declarative models, sessions, and full CRUD using objects instead of raw SQL. | ⬜ Not started | — | — | — |
| Make multi-step database operations all-or-nothing with transactions (commit/rollback), and use constraints and isolation to keep data consistent under concurrency. | ⬜ Not started | — | — | — |
| Model connections between tables — one-to-many and many-to-many — with foreign keys and SQLAlchemy relationships, and query across them with joins. | ⬜ Not started | — | — | — |
| Decouple business logic from data access with a repository layer, so your code depends on an interface (not the ORM) and is easy to test and swap. | ⬜ Not started | — | — | — |
| Use Django's batteries-included ORM: models, the QuerySet API, migrations, relationships, and the admin — contrasting it with SQLAlchemy. | ⬜ Not started | — | — | — |
| Connect to a database and run queries with SQLAlchemy Core: engine, connections, parameterized statements, and the connection lifecycle — the layer the ORM is built on. | ⬜ Not started | — | — | — |
| Diagnose and fix the N+1 query problem — the most common ORM performance bug — using eager loading (joinedload/selectinload) and query inspection. | ⬜ Not started | — | — | — |
| Manage database schema changes with Alembic: generate migrations from model changes, apply and roll them back, and keep environments in sync. | ⬜ Not started | — | — | — |

## Authentication & Security

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Defend against cross-site attacks: configure CORS correctly, protect against CSRF, and apply key web-security headers and input-handling habits. | ⬜ Not started | — | — | — |
| Implement token-based auth in FastAPI: issue a signed JWT on login, protect routes by verifying it, and understand what a JWT is, what it isn't, and where to store it. | ⬜ Not started | — | — | — |
| Store passwords safely: hash with a slow, salted algorithm (bcrypt/argon2), verify on login, and learn why you must never store or encrypt plaintext passwords. | ⬜ Not started | — | — | — |
| Protect endpoints from abuse with per-client rate limiting: implement a limiter, return 429 with the right headers, and understand fixed-window vs token-bucket and why in-memory limits fail at scale. | ⬜ Not started | — | — | — |
| Control what authenticated users can do with role-based access control: assign roles, restrict endpoints by role, deny by default, and keep checks where they can't be bypassed. | ⬜ Not started | — | — | — |
| Implement classic server-side session auth with secure cookies: create a session on login, store it server-side, and set cookies with the right security flags. | ⬜ Not started | — | — | — |
| Let users log in with a third-party provider (a hyperscaler/GitHub) via the OAuth2 authorization-code flow, learning what OAuth delegates and why you never handle the user's provider password. | ⬜ Not started | — | — | — |

## Async & Real-Time

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Do slow work after responding using FastAPI BackgroundTasks — send emails, write logs, process data without making the client wait — and learn its limits. | ⬜ Not started | — | — | — |
| Run durable, scalable background jobs with Celery and a Redis broker: enqueue tasks, process them in separate workers, track status, and handle retries and failures. | ⬜ Not started | — | — | — |
| Write truly async FastAPI endpoints with an async database driver, learning when async helps, the danger of blocking calls in async code, and async sessions. | ⬜ Not started | — | — | — |
| Stream large or generated responses instead of building them fully in memory: StreamingResponse for big files/exports and chunked generation, keeping memory flat. | ⬜ Not started | — | — | — |
| Stream one-way real-time updates from server to client with Server-Sent Events — simpler than WebSockets for live feeds, notifications, and progress updates. | ⬜ Not started | — | — | — |
| Build real-time, bidirectional communication with WebSockets in FastAPI: a chat/broadcast server that pushes messages to connected clients instantly. | ⬜ Not started | — | — | — |
| Speed up expensive reads by caching results in Redis: cache-aside pattern, TTLs, and correct invalidation on writes — the classic performance win with the classic hard problem. | ⬜ Not started | — | — | — |

## Frameworks, Testing & Deployment

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Deploy your containerized app to a reachable URL with a hosted database, production config, and a deploy checklist — the last mile that makes your work real. | ⬜ Not started | — | — | — |
| Build a REST API the Django way with DRF: serializers, viewsets, routers, and the browsable API — getting full CRUD endpoints with minimal code. | ⬜ Not started | — | — | — |
| Build a complete Django app end to end: models, migrations, views, URL routing, templates, and forms — using Django's integrated, convention-driven stack. | ⬜ Not started | — | — | — |
| Test code that uses a database against a real test database with fixtures and per-test isolation (transaction rollback), so tests are realistic yet fast and independent. | ⬜ Not started | — | — | — |
| Make a web app operable: structured request logging, environment-based settings (Pydantic Settings), and basic observability so you can debug production from logs. | ⬜ Not started | — | — | — |
| Build a GraphQL API with Strawberry: define a schema with types, queries, and mutations, and learn how GraphQL differs from REST — and its tradeoffs like the N+1 problem. | ⬜ Not started | — | — | — |
| Write automated tests for a FastAPI app with TestClient and pytest: test endpoints end-to-end, cover success and failure paths, and override dependencies to isolate the unit under test. | ⬜ Not started | — | — | — |
| Package a FastAPI app in Docker and run it with a production ASGI server (uvicorn workers / gunicorn), with multiple workers, health checks, and reverse-proxy awareness. | ⬜ Not started | — | — | — |

---
*Machine-readable proof with commit SHA anchors: [verified-record.json](./verified-record.json)*