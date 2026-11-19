# 7: Loading, Error and Empty States

The backend can be down or slow, and a request can fail. The app has to say what is going on.

## Value Proposition

**As a** user

**I want to** see what the app is doing and what went wrong

**so that** I am never left with a blank page or a button that does nothing.

## Acceptance Criteria

- [ ] **UI:** while the list loads, a loading message is shown.
- [ ] **UI:** when the backend is not reachable, an error message and a button "Try again" replace the list. Nothing crashes. After you start the backend again, "Try again" shows the todos.
- [ ] **UI:** when the API answers an error for add, edit or delete, its message is shown and the list stays as it was.
- [ ] **UI:** after a failed save, the text you typed is still there.
- [ ] **UI:** an empty list shows a friendly message with a hint to add the first todo.
- [ ] **UI:** the "Add" button is disabled while the request runs, so a double click does not create two todos.

## Tasks

- [ ] Stop the backend, reload the page, start the backend, and press "Try again".
- [ ] Add a todo and stop the backend before you press "Add": what does the user see?
