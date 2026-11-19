# 8: Hand Over - Ready for Recap Project 8

In Recap Project 8, you add security and tests to this project. This issue makes sure that someone who has never seen it can start it, and that it can be extended.

## Value Proposition

**As a** developer

**I want to** leave the project documented and clean

**so that** I can start it, understand it and extend it in the next project.

## Acceptance Criteria

- [ ] The `README.md` explains how to start the project from a fresh clone: install, create `backend/.env` from `backend/.env.example`, start the backend and the frontend, and which URLs to open. A classmate can follow it without asking you.
- [ ] `docs/api-contract.md` matches your API: every endpoint and every error. You checked each example in Bruno.
- [ ] `backend/.env.example` lists every variable that the code reads, with placeholders only. No connection string or password is in the repository (search the code and the history).
- [ ] The structure is clean: routes, the model and the error handlers are in separate files, all API calls of the frontend are in `src/api.ts`, and there is no leftover code and no unused file.
- [ ] `npm run typecheck` (backend) and `npm run check` and `npm run build` (frontend) run without errors.
- [ ] In the `README.md`, write two or three sentences on where you would add an owner for each todo (a user who owns it) in the backend and in the frontend.
- [ ] Every user story works end to end in the browser.

## Tasks

- [ ] Ask a classmate to start your project from a fresh clone with only your README.
- [ ] Prepare your demo: add, tick off, edit and delete a todo, and show the error state with the backend stopped.
