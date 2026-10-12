# Project knowledge

## Product summary
The Institute of Computing Lab Reservation System is a browser-based prototype that helps faculty reserve computer labs and lets coordinators review the requests.

## Functional flow
1. A teacher selects a lab, date, and time window.
2. The teacher enters the class purpose and student count.
3. The app validates room capacity and schedule conflicts.
4. The request is saved as Pending.
5. A coordinator can approve or reject it.
6. Cancelled or rejected reservations are handled according to the business rules.

## Business rules
- Reservation dates and times are required.
- A teacher name is required.
- Student count cannot exceed the room capacity.
- A new request cannot overlap with another pending or approved reservation in the same lab on the same date.
- Rejections must include a reason.
- Cancelled bookings become available again for assignment.
- Dashboard counters summarize total and per-status reservations.

## Data model
Each reservation record typically includes:
- reservationId
- teacher
- lab
- date
- startTime
- endTime
- purpose
- studentCount
- status
- rejectionReason (if rejected)
- createdAt / updatedAt

## UI structure
The main page contains:
- top navigation header
- intro copy and lab cards
- totals dashboard
- reservation form
- reservation list with filters
- daily lab schedule viewer

## Prototype limitations
- Data is stored only in browser storage.
- There are no authentication or authorization checks.
- There is no backend persistence or multi-device synchronization.
- This is suitable for demo use only.

## Implementation notes
- The app is static HTML/CSS/JS.
- `script.js` contains most application logic.
- Local storage is the persistence layer for this prototype.
- Validation and rendering logic should stay centralized for easier maintenance.

## Useful reference files
- `README.md` — project summary and usage
- `docs/requirements-analysis.md` — detailed requirements and edge cases
- `docs/ai-prompt-log.md` — AI-assisted project history

## Development approach
Keep changes minimal, domain-accurate, and aligned with the project’s prototype scope. Prefer preserving existing patterns and workflow states over introducing new architectural layers.
