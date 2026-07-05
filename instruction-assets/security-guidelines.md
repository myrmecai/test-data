# Security Guidelines

## Authentication & Authorization
- Never trust client-side checks alone. Always enforce authz on the server.
- Use JWT with short-lived access tokens (15 min) and refresh tokens (7 days).
- Store secrets in the secrets vault, never in source code or env files.

## Input Validation
- Validate all user input at the API boundary.
- Use parameterized queries — never string-concatenate SQL.
- Sanitize HTML output to prevent XSS.

## Dependencies
- Run `npm audit` and `mvn dependency-check` in CI.
- No dependencies with known CVEs in production builds.
- Pin major versions in `package.json` and `pom.xml`.

## Data Protection
- Encrypt credentials at rest (AES-256-GCM).
- Never log sensitive data (passwords, tokens, PII).
- Use HTTPS everywhere. No mixed content.