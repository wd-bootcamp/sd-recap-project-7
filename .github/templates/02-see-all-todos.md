# 2. See All Todos

The first full slice: the todos come from MongoDB, through your API, into the app.

## Value Proposition

**As a** user

**I want to** see all my todos

**so that** I know what I still have to do.

## Acceptance Criteria

- [ ] **Model:** `backend/src/models/Todo.ts` has the schema (`title`: required string, trimmed, `done`: boolean, default `false`), the model and the function `toTodo` that sends `id` instead of `_id` and no `__v`.
- [ ] **API:** `GET /api/todos` (written in `backend/src/app.ts`, below the health route) answers 200 with the list of todos. Every todo has exactly `id`, `title` and `done`.
- [ ] **UI:** the todos are shown as a list. A done todo is shown as done (a checked checkbox and a struck-through title).
- [ ] **UI:** `src/api.ts` has the fetcher, and the list is loaded with `useSWR`. Components do not call `fetch`.

## Tasks

- [ ] Check the endpoint in Bruno first (the list is empty), then fill your database with two or three todos in Atlas or Compass (a todo is `{ "title": "...", "done": false }`) and check again.
- [ ] Open the Network tab in the browser and look at the request to `/api/todos`.
