# Reviewer memory (Lead-owned)

Durable notes the reviewer spawn reloads every run. Per-repo files: `memory/reviewer.<repo>.md`.

Update path is Buzz. Orchestrator records the Buzz message id. Hermes writes this file only after Lead authorization. Policy (X, dimension weights) changes via PR on `adh-meta`, never by a silent patch.

## Standing notes

- X starts at 2.7 / 3. Almost no auto-merges until calibrated.
- Product PRs on `realworld-*`. Harness-issue PRs on `adh` / `adh-meta`.
- One in-flight wave PR per repo.
