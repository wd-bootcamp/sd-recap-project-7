# 6: Delete a Todo

Complete the CRUD operations.

## Value Proposition

**As a** user

**I want to** delete a todo

**so that** my list only has todos that matter.

## Acceptance Criteria

- [ ] **API:** `DELETE /api/todos/:id` answers 204 without a body and removes the todo.
- [ ] **API:** an unknown or invalid `id` answers 404 `{ "error": "Todo not found" }`. Deleting the same todo twice gives 404 the second time.
- [ ] **UI:** every todo has a "Delete" button. The todo is gone from the list after the click.
- [ ] The todo is still gone after a reload of the page, and also in the database.

## Tasks

- [ ] Check the 204 and the 404 in Bruno (send the request twice).
- [ ] A 204 response has **no body**: do not call `response.json()` on it.
