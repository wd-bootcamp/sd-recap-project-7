# 9: Bonus - Filter the Todos

This story is optional. Do it after the core stories.

## Value Proposition

**As a** user

**I want to** show only the open or only the done todos

**so that** I can focus on what is left.

## Acceptance Criteria

- [ ] **API:** `GET /api/todos?done=true` answers only the done todos, `?done=false` only the open ones. Without `done`, all todos are returned.
- [ ] **UI:** three buttons "All", "Open" and "Done" filter the list. The active one is visible.
- [ ] **UI:** the app asks the API for the filtered list (look at the Network tab). It does not filter in the browser.
- [ ] **UI:** an empty result shows a message that fits the filter.
- [ ] `docs/api-contract.md` describes the new query parameter.

## Tasks

- [ ] Check `?done=true`, `?done=false` and no parameter in Bruno.
- [ ] Put the filter into the key of `useSWR`, so that every filter has its own request.
