# API Design Notes

- Use `Idempotency-Key` headers for POST endpoints to handle retries safely.
- Prefer JSON:API-style errors: `{ "errors": [{ "code": "unprocessable_entity", "detail": "..." }] }`.
- Version via URL segment (`/v1/`) only when breaking changes are planned; otherwise use content negotiation.
- Keep controllers thin: validation and persistence logic belongs in service objects.
- For Ruby APIs, dry-validation and dry-monads compose well with Rails.
- Document rate limits and pagination links (`first`, `prev`, `next`, `last`) explicitly.
