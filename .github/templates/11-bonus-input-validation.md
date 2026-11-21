# 11. Bonus: Input Validation

This story is optional. Do it after the core stories, and solve it **with Claude Code**.

## Value Proposition

**As a** user of the API

**I want to** get a clear error for bad input

**so that** no broken data ends up in the database and I know what to fix.

## Acceptance Criteria

- [ ] **API:** `POST /api/todos` with a missing, empty or non-string `title` answers 400 `{ "error": "<message>" }`. A title with only spaces counts as empty.
- [ ] **API:** `PUT /api/todos/:id` answers 400 for an invalid `title`, and for a `done` that is not `true` or `false`.
- [ ] **API:** valid requests work as before. The title is still trimmed.
- [ ] The checks run before the database is touched. They are plain code: no validation library without asking.
- [ ] **UI:** the message of a 400 is shown (see issue 7).
- [ ] `docs/api-contract.md` lists the 400 cases.

## Tasks

- [ ] Set up your security baseline from Recap Project 6 **before** you start Claude Code in this project.
- [ ] Ask Claude Code for a plan in Plan mode. Read it, remove what the story does not ask for, then let it implement. Read the whole diff.
- [ ] Check in Bruno: missing title, empty title, a number as title, `done: "yes"`, and a valid request.

<details>
<summary>Hint ✨</summary>

Never trust `request.body`: anything can arrive there. Check the type with `typeof` before you use a value.

</details>
