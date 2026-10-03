# TASK 010 — SH Install 777

## Status
TODO

## Objective
Allow a user to select a .sh file from accessible storage, stage it through the root backend, and optionally apply explicit 0777 permissions.

## Requirements
- File picker for .sh files.
- Root-mediated staging.
- Preserve file content.
- Explicit permission operation.
- Verify resulting mode.
- Report failures from filesystem, permissions, or SELinux.

## Constraints
- 0777 is never applied implicitly.
- No hidden persistence or auto-execution.
- No fake success.

## Acceptance Criteria
- [ ] Arbitrary user-selected .sh files can be staged.
- [ ] Explicit 0777 operation works when device policy permits.
- [ ] Actual resulting mode is verified.

## Dependencies
- TASK 006
- TASK 009

## Definition of Done
Implementation, device testing, documentation, and commit complete.
