# Documentation Release Process

1. Documentation change requests are tracked as issues in this repository.
2. Every request carries a `Status:` line in its body: `approved` or `deferred`.
3. Only requests that are still open and marked `Status: approved` are applied for the current release.
4. Deferred requests, and requests that are already closed, are left for a future release and must not appear in the public documentation.
5. Approved changes are made on a hotfix branch, committed as a single file change, verified locally, and then published to the remote branch. The `main` branch is never edited directly.
