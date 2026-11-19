# 1: Setup - Run the Starter

The starter has a backend and a frontend that do not know each other yet. In this issue you run both and check that they can talk. No todo feature yet.

## Value Proposition

**As a** developer

**I want to** run the backend and the frontend on my machine, connected to my own database

**so that** every story can build on a working setup.

## Acceptance Criteria

- [ ] You have a MongoDB database (Atlas or local) and `backend/.env` with your `MONGODB_URI`. `.env` is **not** in the repository (check `git status`).
- [ ] `npm run dev` in `backend/` prints that it is connected to the database and that the API is running on port 3001.
- [ ] `GET http://localhost:3001/api/health` answers `{ "status": "ok" }` (check it in Bruno or in the browser).
- [ ] `npm run dev` in `frontend/` shows the page "Todos" on http://localhost:5173.
- [ ] You can explain in one sentence why `backend/src/app.ts` contains `cors(...)`.
- [ ] You read the root `CLAUDE.md` and `docs/api-contract.md`.

## Tasks

- [ ] Create `backend/.env` from `backend/.env.example` and put in your connection string. Use the database name `todos`. **Never paste the connection string into a prompt.**
- [ ] Run `npm i` in `backend/` and in `frontend/`.
- [ ] Start both parts in two terminals.
- [ ] Create a Bruno collection "Todo API" with an environment variable `baseUrl = http://localhost:3001` and a first request for `/api/health`.

<details>
<summary>Hint ✨</summary>

Atlas says "connection refused" or the server stops at start? Check "Network Access" in Atlas (your IP address may have changed) and that the password in the connection string has no special characters that need URL encoding.

</details>
