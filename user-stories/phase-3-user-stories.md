# Phase 3 User Stories

This is the working source of truth for the six stories required in Phase 3. It maps the four existing stories from Phase 1/2 and adds two new mutation-focused stories for the final assignment.

## Story 1: Book a class

- File: `user-story-book-a-class.jpg`
- Goal: As a club member, I want to book an available class so that I can reserve a spot.
- Core flow:
  - Open the home screen and choose an available class.
  - Enter a valid DNI in the booking modal.
  - Submit the booking request.
  - Show loading state while the request is processing.
  - Show success confirmation when the booking completes.
- Mutation type: `POST`
- UI feedback: disabled submit button, error message for invalid DNI, success confirmation.

## Story 2: Report an issue

- File: `user-story-report-an-issue.jpg`
- Goal: As a staff member, I want to report a facility issue so that the club can track and fix it.
- Core flow:
  - Start the issue-report flow from the home screen.
  - Verify identity with DNI.
  - Fill in the issue form with zone, issue type, and description.
  - Submit the report.
  - Show loading state while the request is processing.
  - Show success confirmation with the created ticket number.
- Mutation type: `POST`
- UI feedback: validation warnings, disabled submit button, success confirmation, API error message.

## Story 3: Browse coaches

- File: `user-story-browse-coaches.jpg`
- Goal: As a visitor, I want to browse coaches and open a coach profile so that I can review their background.
- Core flow:
  - Open the coaches page.
  - Load the list of coaches.
  - Open one coach detail page.
  - Show loading and retry behavior if the fetch fails.
- Mutation type: `GET`
- UI feedback: loading text, retryable error state.

## Story 4: Browse venues

- File: `user-story-browse-venues.jpg`
- Goal: As a visitor, I want to browse venues and open venue details so that I can review facility information.
- Core flow:
  - Open the venues page.
  - Load the list of venues.
  - Open one venue detail page.
  - Show loading and retry behavior if the fetch fails.
- Mutation type: `GET`
- UI feedback: loading text, retryable error state.

## Story 5: Update a coach profile

- File: `user-story-update-coach-profile.jpg`
- Goal: As an admin, I want to edit a coach profile so that the directory stays current.
- Core flow:
  - Open a coach detail view.
  - Start an edit action from the profile.
  - Modify fields such as contact info, speciality, or address.
  - Submit the update.
  - Show loading state while saving.
  - Show success confirmation and return to the updated detail view.
- Mutation type: `PUT` or `PATCH`
- UI feedback: validation warnings, disabled submit button, success confirmation, API error message.

## Story 6: Delete an outdated venue note

- File: `user-story-delete-venue-note.jpg`
- Goal: As an admin, I want to delete an outdated venue note so that stale information is removed.
- Core flow:
  - Open a venue detail view or a notes management panel.
  - Choose an outdated note.
  - Confirm the deletion.
  - Show loading state while deleting.
  - Show success confirmation and remove the note from the UI.
- Mutation type: `DELETE`
- UI feedback: confirmation prompt, loading state, success confirmation, API error message.

## Coverage summary

- `GET`: Stories 3 and 4
- `POST`: Stories 1 and 2
- `PUT`/`PATCH`: Story 5
- `DELETE`: Story 6

## Notes

- The four original stories stay recognizable, but now each story shows the write behavior needed for Phase 3.
- The two new stories are intentionally mutation-heavy so the app demonstrates all required HTTP verbs across the six-story set.
- These story files are temporary planning artifacts and can be deleted after the assignment is finished.