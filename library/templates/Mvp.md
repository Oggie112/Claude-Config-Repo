# Before 

# {{PROJECT_NAME}} — MVP Roadmap

> This roadmap is a living document. Update it as scope clarifies.

## Goal

> What does MVP mean for this project? What's the minimum that delivers value?

## Milestones

### M1 — Foundation
- [ ] Project scaffold
- [ ] CI/CD pipeline
- [ ] Auth (if applicable)

### M2 — Core Features
- [ ] TBD

### M3 — Launch Ready
- [ ] Testing coverage
- [ ] Documentation
- [ ] Deployment

## Out of Scope (for MVP)

> Explicitly list what you're deferring to avoid scope creep.

# After

# C58 — MVP Roadmap

> This roadmap is a living document. Update it as scope clarifies.

## Goal

A working backend that pulls event data from Sanity and exposes it to a frontend, with enough structure that a non-technical client can manage content themselves.

## Milestones

### M1 — Foundation
- [ ] Next.js + TypeScript scaffold
- [ ] Sanity studio configured and deployed
- [ ] Sanity schema: Event, Venue, Category
- [ ] Environment variables and local dev working

### M2 — Core Features
- [ ] API routes consuming Sanity data
- [ ] Event listing and detail endpoints
- [ ] Basic filtering (date, category)
- [ ] Jest test coverage for API routes

### M3 — Launch Ready
- [ ] Error handling and edge cases
- [ ] Documentation for client CMS usage
- [ ] Deployment (Vercel recommended for Next.js)

## Out of Scope (for MVP)

- Authentication / ticketing
- Payment processing
- Email notifications
- Analytics