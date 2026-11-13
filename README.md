# ascout-c1c-proof

A test repository for Ascout's C1c: the live proof of the GitHub App check gate described in
[C1_GITHUB_APP_GATE_DESIGN.md](https://github.com/TheHalfMoon/Ascout/blob/main/specs/017-unified-assurance/C1_GITHUB_APP_GATE_DESIGN.md).
It is not a product. Its PRs include deliberate attempts to forge the check and to read the App key.

- `Ascout PR Collect` runs on pull requests with a read-only token and no secrets, using the
  released Ascout v0.3.0 (SHA-256 checked).
- `Ascout PR Publish` runs on `workflow_run` from `main` in the `ascout-publish` environment, which
  only `main` can use, and posts the **Ascout verification** check as this repository's GitHub App.
