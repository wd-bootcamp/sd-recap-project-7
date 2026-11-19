# 5: Edit a Todo

Change the title of a todo. The API route is the one from issue 4.

## Value Proposition

**As a** user

**I want to** change the title of a todo

**so that** I can fix a typo or a changed plan.

## Acceptance Criteria

- [ ] **UI:** every todo has an "Edit" button. It turns the title into a text field with the buttons "Save" and "Cancel".
- [ ] **UI:** "Save" sends the new title (and keeps the `done` state). The todo shows the new title.
- [ ] **UI:** "Cancel" closes the field and keeps the old title.
- [ ] **UI:** an empty title is not sent.
- [ ] The new title is still there after a reload of the page.

## Tasks

- [ ] Use the existing `updateTodo` function and the existing route. This story needs no change in the backend.
- [ ] Try it with an empty title and see what happens.
