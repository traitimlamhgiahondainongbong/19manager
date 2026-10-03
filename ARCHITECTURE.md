# 19Manager Architecture

## Principles

1. UI must not directly perform privileged operations.
2. Privileged operations go through a controlled root backend.
3. Root operations must return real success/failure information.
4. Never claim success when the kernel, SELinux, permissions, or root policy rejected an operation.
5. File paths and shell arguments must be validated.
6. IPC contracts must be explicit and versionable.
7. Sensitive logs must avoid unnecessary data exposure.

## Planned layers

- Presentation: Android UI and navigation
- Domain: file/package/script operations and validation
- Root backend: RootManager / RootService
- IPC: Binder/AIDL or an equivalent versioned IPC contract
- Root integration: Magisk / KernelSU / APatch compatible entrypoints
- Storage: filesystem and package-data operations

## Privileged filesystem scope

The implementation is expected to support legitimate administration of paths such as:

- /data
- /data/adb
- /system
- /vendor
- /product
- /apex

Operations include browse, copy, move, delete, rename, mkdir, read, write, chmod, and chown, subject to actual device permissions and security policy.

## Security

No path traversal, command injection, fake permission elevation, or hidden privileged behavior.
