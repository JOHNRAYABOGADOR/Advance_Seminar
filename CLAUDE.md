# CLAUDE.md

## Repository intent
This project is a static prototype for a university computer lab reservation workflow. The user experience is implemented entirely in the browser and stores data locally.

## How to use this repository
1. Open `index.html` in a browser to use the application.
2. Interact with the reservation form to create, approve, reject, or cancel requests.
3. Use the filter controls and schedule panel to review bookings.

## Domain model
- Lab: Comlab 1, Comlab 2, or AES.
- Capacity: 40, 30, and 25 students respectively.
- Reservation status: Pending, Approved, Rejected, Cancelled.
- Time conflict checks apply to same lab + same date + overlapping periods.

## Known technical constraints
- No package manager, build system, or server is required.
- Data is stored in localStorage only.
- The UI is driven by `script.js` with DOM updates.
- This app is designed for prototype/demo work, not production deployment.

## File responsibility map
- `index.html` — page skeleton and all form fields.
- `style.css` — theme, layout, responsiveness, and control styling.
- `script.js` — state management, validation, schedule logic, and filtering.
- `docs/requirements-analysis.md` — detailed functional and edge-case requirements.

## Coding expectations
- Keep code readable and easy to reason about.
- Prefer direct DOM manipulation and lightweight JavaScript patterns already used in the project.
- Retain consistent naming and status handling across the reservation workflow.
- If you change business rules, make sure the docs remain aligned.

## Quick validation
For a manual validation pass, create a reservation, verify seat capacity rules, test overlap prevention, confirm status transitions, and check the schedule view after approval or cancellation.
