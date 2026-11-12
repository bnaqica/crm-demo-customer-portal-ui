# Spec Delta

## Purpose

Lets external users sign in, register and recover access through the `portal` realm only.

## ADDED Requirements

### Requirement: Login and registration
The landing page SHALL offer Sign in and Register, both using Authorization Code with PKCE against the `portal` realm; Register SHALL open Keycloak's registration page.

#### Scenario: Register
- **WHEN** a visitor clicks Register
- **THEN** Keycloak's `portal` registration page opens

### Requirement: Verified email
A signed-in user whose email is not verified SHALL see only a verify-your-email page with a resend option.

#### Scenario: Unverified
- **WHEN** a user with `email_verified` false signs in
- **THEN** only the verify-your-email page is shown

### Requirement: Tokens in memory
Tokens SHALL be held in memory only, and Sign out SHALL end the Keycloak session.

#### Scenario: Sign out
- **WHEN** a user signs out
- **THEN** the session ends and the landing page is shown
