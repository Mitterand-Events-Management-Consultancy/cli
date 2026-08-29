# Repository Audit

## Finding

This repository is a fork of `npm/cli`, the npm JavaScript package manager. It is not an original application foundation for VaultCore, Mitterand Pay, or the proposed superagent platform.

## Decision

Do not repurpose this repository as the production application codebase. Preserve it as an upstream fork/reference unless there is a specific, documented reason to maintain modifications.

## Immediate controls

- Changes should be made through pull requests.
- Dependency changes are reviewed before merge.
- Existing upstream CI, release, and CodeQL workflows should be preserved unless a specific failure or incompatibility is identified.
- Repository settings should enforce least privilege, protected branches, and required checks.

## Product repository strategy

Create dedicated repositories for first-party products rather than mixing proprietary application code into an upstream fork:

1. product/platform application
2. backend and API services
3. infrastructure and deployment configuration
4. security and architecture documentation

## Merge policy

No direct production changes should be made merely because an automated tool can write to the repository. Every change must have a clear purpose, validation evidence, and rollback path.
