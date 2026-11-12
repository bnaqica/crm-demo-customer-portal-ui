# Spec Delta

## Purpose

Shows portal users the features of their tier and explains when more will become available.

## ADDED Requirements

### Requirement: Tier from the backend
After sign-in the app SHALL load `/me` and show navigation for the features it lists.

#### Scenario: Starter navigation
- **WHEN** a starter signs in
- **THEN** only starter features appear in navigation

### Requirement: Upgrade notice
Starters SHALL see a notice that more features become available once their account is reviewed; standard users SHALL NOT see it.

#### Scenario: Promoted user
- **WHEN** a promoted user signs in
- **THEN** no upgrade notice is shown

### Requirement: Server denial respected
A 403 from the backend SHALL show a not-available message and reload `/me`.

#### Scenario: Tier changed
- **WHEN** an action returns 403
- **THEN** a not-available message is shown and the profile is reloaded
