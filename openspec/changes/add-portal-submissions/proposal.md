# Proposal

## Why

Standard portal users submit data and documents and follow their status; this is the portal's main purpose.

## What Changes

- My submissions list and detail with status and rejection reason.
- New submission form with document upload through pre-signed URLs and scan status.
- Correct a submission by creating a new version.

## Capabilities

### New Capabilities
- `portal-submission-ui`: portal screens for submissions and documents.

## Impact

- Uses portal backend submissions and document-upload endpoints. Depends on `bootstrap-portal-app`. Object storage must allow CORS PUT from the portal origin.
