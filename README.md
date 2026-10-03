# 19Manager

Root-capable Android file manager and system management application.

## Project goals

19Manager is designed as a real production-oriented Android application with a privileged root backend. The project targets legitimate device administration and file-management workflows.

Core areas:
- Modern Android file manager UI
- RootService and IPC
- Root filesystem operations
- Package Explorer
- SH Manager
- SH installation/staging with explicit permissions
- Terminal
- Archive management
- Search
- Magisk / KernelSU / APatch compatibility
- Diagnostics, logging, testing, and security validation

## Development workflow

The repository is driven by ordered task specifications in tasks/.

The development agent must:
1. Read CLAUDE.md, PROJECT_STATUS.md, ARCHITECTURE.md, and FILE_INVENTORY.md.
2. Select the first unfinished task whose dependencies are satisfied.
3. Implement that task completely.
4. Build and test it.
5. Update project documentation and status.
6. Commit the completed work.
7. Do not begin the next task unless explicitly instructed.

## Repository structure

- app/ — Android application
- root-module/ — privileged/root integration
- tasks/ — ordered implementation specifications
- docs/ — technical documentation
- PROJECT_STATUS.md — current project state
- FILE_INVENTORY.md — tracked project files
- ARCHITECTURE.md — architecture contract
- CLAUDE.md — autonomous development contract