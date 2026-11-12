# Design

## Decisions

- Upload with `fetch` PUT to the pre-signed URL (no token sent to storage), with `XMLHttpRequest` only where progress is needed.
- Scan status polled every 3 seconds until CLEAN or INFECTED, stopping after 2 minutes with a retry option.
- Type and size limits read from the backend so client and server rules match; the backend still enforces them.
