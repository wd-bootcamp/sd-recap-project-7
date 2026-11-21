# 12. Bonus: Error Handling

This story is optional. Do it after the core stories, and solve it **with Claude Code**.

## Value Proposition

**As a** user of the API

**I want to** get the same kind of answer for every error

**so that** the app can show a message instead of crashing, and nothing internal leaks.

## Acceptance Criteria

- [ ] **API:** a request to an unknown route answers 404 `{ "error": "Not found" }`.
- [ ] **API:** a body that is not valid JSON answers 400 `{ "error": "<message>" }`.
- [ ] **API:** an `id` like `abc` answers 404 `{ "error": "Todo not found" }`, not 500.
- [ ] **API:** an unexpected error answers 500 `{ "error": "Internal server error" }`. The details are logged on the server and never sent to the client.
- [ ] The handlers are in `backend/src/middleware/errors.ts` and are registered last in `app.ts`. The routes have no `try/catch`: Express 5 forwards errors of `async` handlers on its own.
- [ ] `docs/api-contract.md` lists the cases.

## Tasks

- [ ] Set up your security baseline from Recap Project 6 **before** you start Claude Code in this project.
- [ ] Ask Claude Code for a plan in Plan mode. Read it, remove what the story does not ask for, then let it implement. Read the whole diff.
- [ ] Check in Bruno: an unknown route, a broken JSON body, `/api/todos/abc`.

<details>
<summary>Hint ✨</summary>

An error handler is a middleware with **four** parameters (`err`, `request`, `response`, `next`). `express.json()` throws a `SyntaxError` with `status` 400 for invalid JSON, and mongoose throws a `CastError` for an id it cannot turn into an ObjectId.

</details>
