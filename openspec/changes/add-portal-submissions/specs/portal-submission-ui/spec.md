# Spec Delta

## Purpose

Lets external users submit data and documents and follow what happened to their own submissions.

## ADDED Requirements

### Requirement: My submissions
The app SHALL list the user's own submissions with type, created time and status, and show a submission's versions, documents, status and rejection reason.

#### Scenario: Rejected shown
- **WHEN** a user opens a rejected submission
- **THEN** status REJECTED and the reason are shown

### Requirement: Upload documents
The app SHALL upload files directly to storage using the pre-signed URL, check type and size before uploading, and show each document's progress and scan status.

#### Scenario: File too large
- **WHEN** a user picks a file over the size limit
- **THEN** an error is shown and no upload starts

#### Scenario: Infected file
- **WHEN** a document's scan status becomes INFECTED
- **THEN** the document is shown as rejected and can't be attached

### Requirement: Submit
The form SHALL enable Submit only when required fields are filled and every attached document is CLEAN.

#### Scenario: Scan pending
- **WHEN** an attached document is still being scanned
- **THEN** Submit is disabled with a waiting message

### Requirement: Correct a submission
The owner SHALL be able to correct a submission, which opens a pre-filled form and creates a new version; earlier versions stay viewable and unchanged.

#### Scenario: Correction
- **WHEN** a user submits a correction
- **THEN** the submission shows version 2 as current and version 1 in its history
