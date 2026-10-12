---
name: project-knowledge
description: "Use this skill when you need project context, repository conventions, or the domain rules for the Institute of Computing lab reservation prototype."
---

# Project Knowledge Skill

## Purpose
Use this skill to quickly understand the repository's goals, the main application flow, and the project-specific rules that should be preserved during changes.

## Project overview
This repository contains a static browser-based prototype for managing computer lab reservations. Faculty members submit booking requests, coordinators review and approve or reject them, and users can filter records and inspect a daily lab schedule.

## Core application facts
- The app runs as a front-end prototype with HTML, CSS, and JavaScript.
- The main entry point is `index.html`.
- Reservation data is stored in browser `localStorage`.
- There is no backend, authentication, or multi-user synchronization.
- The three labs are Comlab 1 (40 seats), Comlab 2 (30 seats), and AES (25 seats).

## Reservation rules to preserve
- A reservation requires a teacher name, lab, date, start time, end time, purpose, and student count.
- Student count must not exceed the selected lab capacity.
- Pending and approved reservations cannot overlap on the same lab and date.
- Rejected reservations require a reason.
- Cancelled reservations make the slot available again.
- Dashboard totals and filters should reflect the current status set.

## Important files
- `index.html` — page layout and form structure.
- `style.css` — styling and responsive layout.
- `script.js` — booking logic, validation, filters, dashboard data, and schedule rendering.
- `README.md` — high-level project description and usage.
- `AGENTS.md` — repository-wide guidance for AI-oriented work.
- `docs/requirements-analysis.md` — detailed requirements and business rules.

## Working guidance
- Keep changes focused and consistent with the prototype scope.
- Prefer minimal edits over broad refactors.
- Preserve browser-only behavior and localStorage-based state management.
- If business rules change, update the relevant documentation to match the new behavior.
- Manual validation should include creating a reservation, checking capacity, testing overlap prevention, and verifying status transitions.
