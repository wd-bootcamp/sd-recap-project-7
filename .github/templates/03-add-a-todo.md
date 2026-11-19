# 3: Add a Todo

Create a todo through the app.

## Value Proposition

**As a** user

**I want to** add a todo

**so that** I do not forget what I have to do.

## Acceptance Criteria

- [ ] **API:** `POST /api/todos` with `{ "title": "..." }` answers 201 with the new todo (`done` is `false`). The title is trimmed.
- [ ] **API:** a missing or empty title answers 400 `{ "error": "<message>" }`. A body that is not valid JSON answers 400, too.
- [ ] **UI:** a form with a text field and an "Add" button is shown above the list.
- [ ] **UI:** the form does not send an empty title (the button is disabled or a message is shown).
- [ ] **UI:** after saving, the field is empty and the new todo is in the list.
- [ ] The new todo is still there after a reload of the page, and you see it in the database.

## Tasks

- [ ] Check the 201 and the 400 cases in Bruno. Look at the response body, not only at the status code.
- [ ] The API call is a function in `src/api.ts`.
- [ ] After the request, tell SWR to load the list again (`mutate`).

<details>
<summary>Hint ✨</summary>

Send `Content-Type: application/json` and a `JSON.stringify`d body with `fetch`, otherwise `express.json()` does not read the body.

</details>
