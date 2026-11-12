# Proposal

## Why

External users use only the portal web app, signing in to the `portal` realm by invitation or self-registration. Starters get minimal features until the CRM promotes them.

## What Changes

- New React + TypeScript + Vite app with lint, test, build and CI.
- OIDC Authorization Code + PKCE to realm `portal`, client `portal-app`; Register and Forgot password links to Keycloak's flows (CAPTCHA, email verification, MFA handled there).
- Profile from portal backend `GET /me`; starter vs standard tier drives navigation and an upgrade-pending notice.

## Capabilities

### New Capabilities
- `portal-authentication`: signing in, registering and signing out.
- `portal-tiers`: what starters and standard users see.

## Impact

- Dev server on port 5174; portal backend URL `VITE_PORTAL_BASE_URL` (default `http://localhost:8082`); backend must allow CORS from this origin.
