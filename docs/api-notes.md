# API Design Notes

- Prefer explicit resource endpoints over action verbs.
- Use consistent error shapes: `{ error: { code, message } }`.
- Version via URL prefix (`/v1/`) or header — pick one and document it.
- Idempotency keys for POST/PATCH where clients may retry.
- Rate limit headers: `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset`.

## To explore
- OpenAPI 3.1 vs 3.0 differences for `nullable`.
- JSON:API sparse fieldsets vs GraphQL-style field selection.