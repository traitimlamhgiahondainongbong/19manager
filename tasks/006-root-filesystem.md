# TASK 006 — Root Filesystem

## Status
TODO

## Objective
Implement real root filesystem operations through the backend.

## Requirements
- Browse filesystem.
- Copy, move, delete, rename.
- mkdir.
- Read/write.
- chmod/chown.
- Actual error reporting.
- SELinux and permission-denied diagnostics.

## Constraints
- Validate paths.
- No shell injection.
- Never report success before the operation actually succeeds.
- 0777 must only be applied when explicitly requested.

## Acceptance Criteria
- [ ] Core operations work on a rooted test device.
- [ ] Failures are accurately surfaced.
- [ ] Security validation exists.

## Dependencies
- TASK 005

## Definition of Done
Implementation, tests, documentation, and commit complete.
