# Design

## Decisions

- Same stack as the other UIs: Vite, React 19, TypeScript strict, React Router, TanStack Query, `react-oidc-context` with in-memory storage, Vitest + RTL + MSW, Playwright.
- Register uses the OIDC `prompt=create` parameter so registration stays inside Keycloak (CAPTCHA, rate limits and corporate-domain rejection are realm configuration).
- Public-facing styling and accessibility (WCAG 2.2 AA) from the start, as this app faces customers.
