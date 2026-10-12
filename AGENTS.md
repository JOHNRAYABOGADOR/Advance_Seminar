# AGENTS.md

## Project overview
This repository contains a static browser prototype for the Institute of Computing lab reservation system. It allows faculty to submit lab booking requests, coordinators to approve or reject them, and users to view filtered records and a daily lab schedule.

## Core purpose
- Manage computer lab reservations for Comlab 1, Comlab 2, and AES.
- Prevent overlapping bookings for the same lab and date.
- Enforce room capacity based on selected lab.
- Track reservation status: Pending, Approved, Rejected, and Cancelled.
- Store all data in browser localStorage for this prototype.

## Important project facts
- The app is a front-end-only project; there is no backend or database.
- Run the app by opening `index.html` in a modern browser.
- No install step or build tool is required.
- The project intentionally prioritizes prototype behavior over production security or authentication.

## Key files
- `index.html` — UI structure and form layout.
- `style.css` — visual styling and responsive layout.
- `script.js` — reservation logic, validation, status changes, filtering, dashboard totals, and schedule rendering.
- `README.md` — high-level overview and feature summary.
- `docs/requirements-analysis.md` — business rules and project requirements.
- `docs/ai-prompt-log.md` — development history and AI-generated prompt notes.

## Working rules for agents
- Prefer surgical edits to existing logic rather than large rewrites.
- Preserve browser-only behavior and localStorage-driven state.
- Keep project scope limited to the prototype; do not add backend services unless explicitly requested.
- If changing reservation rules, update the requirements or documentation that describe the behavior.
- Validate changes by running the app in a browser and checking the affected reservation flows.

## Reservation rules to preserve
- A reservation has teacher name, lab, date, start time, end time, purpose, and student count.
- Student count must be within the capacity of the chosen lab.
- Pending and Approved reservations cannot overlap in the same lab and date.
- Rejected reservations require a reason.
- Cancelled reservations reopen the time slot for new bookings.
- Filters should continue to support teacher, lab, date, and status searches.

## Notes for future work
This project is best treated as a front-end prototype. If future versions need real coordination or multi-user functionality, a shared backend, authentication, and concurrency-safe booking rules will be required.
