# Asonja Taiwo Omotayo

**Backend Engineer** · Node.js, TypeScript and PostgreSQL · Lagos, Nigeria

I build backend systems where correctness is not negotiable. My work sits around money movement, concurrency and failure handling: the parts of a system that behave fine in development and fail quietly in production.

First Class B.Eng in Mechanical Engineering and an M.Eng in Manufacturing and Automation, with three peer reviewed publications in modelling and optimisation. That background is why I reach for invariants and proofs before I reach for a framework.

---

## What I do well

**Correctness under concurrency.** Preventing the races that only appear under real load: overdrafts from read then compare, duplicated money movement from retried requests, lost updates between simultaneous writers. I solve these with row level locking, database enforced invariants and deterministic lock ordering rather than application side checks that hold only on the paths someone remembered to route through.

**Designing for failure, not the happy path.** Idempotency keys with leases that survive a process dying mid request. Retry with exponential backoff, dead lettering and operator replay. Reconciliation for the event that never arrives. Compensating actions where a rollback is impossible because the money already moved.

**Data integrity at the database layer.** Append only history, constraint and lifecycle triggers, deferred constraint checking, state machines enforced in SQL, and independent drift detection that recomputes derived state from source. An invariant enforced only in application code is a convention, not a guarantee.

**API and service design.** REST APIs with explicit transaction boundaries, structured machine readable error codes, keyset pagination, OpenAPI documentation, and authentication and authorisation that fails closed by default.

**Testing that proves the claim.** Suites run against real database semantics rather than mocks, covering concurrency races, duplicate delivery, crashed handlers and deliberate corruption. If a guarantee is not attacked by a test, I do not claim it.

---

## Stack

**Languages** TypeScript, JavaScript, C#, Python, SQL

**Backend** Node.js, NestJS, Express, REST API design, JWT and OAuth2, role based access control, background jobs, webhook processing, third party integrations

**Databases** PostgreSQL, MongoDB, MySQL, PL/pgSQL, triggers and constraints, transaction isolation, row level locking, schema design, indexing, query optimisation

**Practice** Double entry ledger design, idempotency, reconciliation, concurrency control, automated testing with Vitest and Jest, OpenAPI and Swagger, code review

**Infrastructure** Docker, Docker Compose, CI/CD, GitHub Actions, AWS, Azure, Netlify, Vercel

**Frontend** React, responsive and mobile first design, Tailwind CSS

**Working with AI** Structured and spec driven prompting as part of the delivery workflow, used for scaffolding, refactoring, review and documentation, with design decisions and shipped code staying mine.

---

## Beyond code

Co-Founder and COO at **Dronavid**, a drone logistics venture targeting last mile delivery in emerging African markets. I own operational strategy, product definition and technical feasibility, which keeps me close to why a system is being built and not only how.

Currently building a payout orchestration service in .NET: transactional outbox, consumer side inbox, saga compensation and poison message handling.

---

## Reach me

[asonjataiwo@gmail.com](mailto:asonjataiwo@gmail.com) · [LinkedIn](https://www.linkedin.com/in/asonja) · [asonja.com.ng](https://www.asonja.com.ng)

Open to backend engineering roles, remote or Lagos based. Pinned repositories below.
