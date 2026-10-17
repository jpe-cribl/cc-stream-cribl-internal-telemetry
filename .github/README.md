# `.github/` — workflow callers

This repository calls the shared Cribl pack workflows in `jpe-cribl/.github`.
Pin each reusable workflow to a full commit SHA and include a ref comment, such
as `# main`. The shared workflows run the scripts from `jpe-cribl/.github` in
CI, checked out under `.gh-shared/`.

## Caller workflows

- `workflows/test.yml` calls the shared pack validation and test workflow.
- `workflows/release.yml` calls the central release workflow and the shared
  pack release workflow.
- `workflows/e2e.yml` calls the shared end-to-end workflow.
