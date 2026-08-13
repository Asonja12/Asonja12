# Asonja Taiwo Omotayo

**Backend Engineer** · Node.js, TypeScript and PostgreSQL · Lagos, Nigeria

I build backend systems where correctness is not negotiable. Most of my work sits around money movement, concurrency and failure handling: the parts of a system that behave fine in development and fail quietly in production.

I hold a First Class B.Eng in Mechanical Engineering and an M.Eng in Manufacturing and Automation from Nanjing University of Science and Technology, with three peer reviewed publications in modelling and optimisation. That background is why I tend to reach for invariants and proofs before I reach for a framework.

---

## Featured work

### [Payment Ledger](https://github.com/Asonja12/payment-ledger) · a financial transaction engine

A wallet and payments backend built the way money actually has to be handled. Double entry accounting, idempotent money movement, webhook driven reconciliation, and concurrency control enforced by PostgreSQL rather than by application code.

Most wallet implementations are a `balance` column and an `UPDATE`. That design fails quietly: two concurrent withdrawals both see sufficient funds, a redelivered webhook credits twice, a crashed process leaves money in neither account. This project is a working answer to what it takes to build the version that does not do that.

- Financial invariants enforced as database triggers and constraints, so they hold for every writer including a `psql` session at 3am
- Concurrent overdraft prevented by a row lock acquired inside a `BEFORE INSERT` trigger, with no read then compare anywhere on the spending path
- Lease based idempotency that survives a process dying mid request, without ever reclaiming a completed key
- Webhook pipeline that distinguishes an event already finished from one merely seen, because providers redeliver precisely when processing failed
- Pull based reconciliation that heals missing webhooks and deliberately refuses to auto resolve amount mismatches
- 159 tests against real PostgreSQL semantics, no database mocking, including concurrency races, crashed handlers and deliberate data corruption

`NestJS` `TypeScript` `PostgreSQL` `PL/pgSQL` `Docker` `Vitest`

### [Bojamiley CRM](https://github.com/Asonja12/BojamileyCRM) · fashion house operations platform

A multi tenant CRM in production use by a Lagos luxury fashion house, unifying client records, bespoke measurements, order pipelines, payment tracking and inventory.

- JWT authentication with an admin approval gate, so new registrations stay locked until authorised
- Role based access control separating the internal admin workspace from a client portal scoped to a single customer
- MongoDB schemas linking measurement profiles to repeat orders, removing re-measurement for returning clients

`React` `Node.js` `Express` `MongoDB` `JWT`

### Currently building

A **payout orchestration service in .NET**, solving the limitation my ledger states honestly in its own README: its background workers are in-process timers rather than a queue runtime. Transactional outbox, consumer side inbox, saga compensation and poison message handling, with ASP.NET Core, MassTransit, RabbitMQ and Testcontainers.

---

## Stack

**Languages** TypeScript, JavaScript, C#, Python, SQL

**Backend** Node.js, NestJS, Express, REST API design, JWT and OAuth2, role based access control, background jobs, third party integrations

**Databases** PostgreSQL, MongoDB, MySQL, PL/pgSQL, triggers and constraints, transaction isolation, row level locking, schema design, indexing

**Practice** Double entry ledger design, idempotency, webhook processing, reconciliation, concurrency control, automated testing with Vitest and Jest, OpenAPI

**Infrastructure** Docker, CI/CD, GitHub Actions, AWS, Azure, Netlify, Vercel

**Frontend** React, responsive and mobile first design, Tailwind CSS

---

## Also

Co-Founder and COO at **Dronavid**, a drone logistics venture targeting last mile delivery in emerging African markets. I own operational strategy, product definition and technical feasibility, and I built and deployed the company platform.

---

## Reach me

[asonjataiwo@gmail.com](mailto:asonjataiwo@gmail.com) · [LinkedIn](https://www.linkedin.com/in/asonja) · [asonja.com.ng](https://www.asonja.com.ng)

Open to backend engineering roles, remote or Lagos based.
