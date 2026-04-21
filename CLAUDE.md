# Odd Duck Labs — Project Guidelines

## Project Overview

Static landing page for Odd Duck Labs, hosted on GitHub Pages at oddducklabs.com. Single `index.html` file with inline CSS/JS.

## Security Rules

- Never hardcode secrets, API keys, tokens, or passwords. Always use environment variables. Never bundle secrets into front-end code.
- All external API calls must go through edge/serverless functions — never call third-party APIs directly from client-side code.
- Sanitize and validate all user inputs. Reject oversized or malformed payloads.
- All API endpoints must have rate limiting. Authentication routes are limited to 5 attempts per IP per 15 minutes.
- CORS must use explicit allowed origins — never use wildcard `*` in production. Scope allowed methods and headers to only what is needed.
- Follow OWASP Top 10 guidelines. All new endpoints and features must be reviewed for injection, XSS, CSRF, IDOR, and other common vulnerabilities.
