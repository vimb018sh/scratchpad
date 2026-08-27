# API Design Notes

Some principles I keep coming back to:

- Prefer RESTful resources over actions.
- Use consistent error shapes: `{ "error": { "code": "...", "message": "..." } }`.
- Version via URL segment (`/v1/`) unless the team chooses headers.
- Always paginate list endpoints; default 25 per page.
- Use `422 Unprocessable Entity` for validation failures.
- Document with OpenAPI and keep the spec in sync in CI.
- Timestamps should be UTC ISO 8601.
