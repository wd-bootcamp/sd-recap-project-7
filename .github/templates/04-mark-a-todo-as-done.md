# 4. Mark a Todo as Done

Update a todo.

## Value Proposition

**As a** user

**I want to** tick off a todo, and untick it again

**so that** I can see what is done and what is not.

## Acceptance Criteria

- [ ] **API:** `PUT /api/todos/:id` with `{ "title": "...", "done": true }` replaces the todo and answers 200 with the updated todo (the new values, not the old ones).
- [ ] **API:** an unknown `id` (a valid ObjectId that is not in the database) answers 404 `{ "error": "Todo not found" }`.
- [ ] **UI:** every todo has a checkbox. Clicking it sends the request and the todo changes in the list.
- [ ] The state is still the same after a reload of the page.

## Tasks

- [ ] Check the 200 and the 404 case in Bruno.
- [ ] `PUT` replaces the whole todo: send the current `title` together with the new `done`.

<details>
<summary>Hint ✨</summary>

`findByIdAndUpdate` returns the **old** document unless you pass `returnDocument: "after"`.

</details>
