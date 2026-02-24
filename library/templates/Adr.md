# Before

# Architecture Decision Records

ADRs are created by  project init and added manually as significant decisions are made.

| # | Title | Status |
|---|-------|--------|
| 001 | Initial tech stack | — |

---

# After

ADR 001 — Initial Tech Stack
Date: 2026-02-24
Status: Accepted
Context
C58 is a backend for a non-technical client's event business. The priority is speed of development, low maintenance overhead, and a CMS the client can manage without developer involvement. The project starts as a rapid prototype.
Decision
Next.js + React + TypeScript for the application layer. Next.js API routes give us a backend without a separate server, and the React ecosystem is well-supported for future frontend needs if required.
Sanity as the CMS and primary data layer. Sanity Studio gives the client a clean, customisable editing interface. No separate database needed at this stage — Sanity handles persistence, querying (GROQ), and CDN delivery.
Tailwind CSS for styling, included for consistency with likely frontend work ahead.
Jest for testing. Familiar, well-documented, integrates cleanly with Next.js. Noted as an area to build confidence in during development.
npm as package manager for simplicity and universal compatibility.
Consequences

No separate database to manage — reduces ops burden significantly for a prototype
Sanity has a free tier that covers early-stage usage
If data needs grow complex (relational data, transactions), Sanity may need to be supplemented or replaced
Jest coverage on API routes is a goal for M2 — invest time here to build testing confidence
