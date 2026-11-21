# 10. Bonus: Move the Routes into a Router

This story is optional. Do it after the core stories, and solve it **with Claude Code**.

## Value Proposition

**As a** developer

**I want to** have the todo routes in their own file

**so that** `app.ts` stays small and the routes are easy to find, test and extend.

## Acceptance Criteria

- [ ] `backend/src/routes/todos.ts` exports a `todosRouter` (an Express `Router`) with all four todo routes.
- [ ] `backend/src/app.ts` only has CORS, the JSON parser, the health route and `app.use("/api/todos", todosRouter)`. It still exports `app` and does not listen.
- [ ] The API behaves exactly as before: every request in your Bruno collection gives the same answer, and the app works in the browser.
- [ ] Only `app.ts` and `routes/todos.ts` changed, and there is no new dependency.
- [ ] You can explain what `Router` does, and why the paths in the router no longer start with `/api/todos`.

## Tasks

- [ ] Set up your security baseline from Recap Project 6 **before** you start Claude Code in this project.
- [ ] Ask Claude Code for a plan in Plan mode. Read it and remove everything the story does not ask for, then let it implement. Read the whole diff.
- [ ] Run all Bruno requests again.

<details>
<summary>Hint ✨</summary>

When the router is mounted on `/api/todos`, a route written as `router.get("/")` answers `GET /api/todos`, and `router.put("/:id")` answers `PUT /api/todos/:id`.

</details>
