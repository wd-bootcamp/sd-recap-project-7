# 4: Mark a Todo as Done

Update a todo.

## Value Proposition

**As a** user

**I want to** tick off a todo, and untick it again

**so that** I can see what is done and what is not.

## Acceptance Criteria

- [ ] **API:** `PUT /api/todos/:id` with `{ "title": "...", "done": true }` replaces the todo and answers 200 with the updated todo (the new values, not the old ones).
- [ ] **API:** an unknown `id` answers 404 `{ "error": "Todo not found" }`. An `id` like `abc` answers 404, too, not 500.
- [ ] **API:** an empty title answers 400, also for `PUT`.
- [ ] **UI:** every todo has a checkbox. Clicking it sends the request and the todo changes in the list.
- [ ] The state is still the same after a reload of the page.

## Tasks

- [ ] Check the 200, 404 (unknown and invalid id) and 400 cases in Bruno.
- [ ] `PUT` replaces the whole todo: send the current `title` together with the new `done`.

<details>
<summary>Hint ✨</summary>

`findByIdAndUpdate` returns the **old** document unless you pass `returnDocument: "after"`. An update also skips the schema rules unless you pass `runValidators: true`.

</details>
