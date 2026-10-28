# INIT-ADH-000 — Agentic Delivery Harness G0

Status: stub (filed from locked programme rules; not yet Hermes-authored).
Board: [ADH](https://github.com/orgs/drivestream-lab/projects/4).
Epic: `[feature] INIT-ADH-000 — Agentic Delivery Harness G0` on `adh-meta`.

## Objective

Mimic a senior PM and a senior developer delivering a programme — with data, not heroics. GitHub PRs are delivery. Buzz is the conversation plane. Hermes is the autonomous LLM (PM lane + after-PR verify/grade/RCA). Cursor CLI is the wave implementer.

## Identities

| Identity | Kind | Role |
| --- | --- | --- |
| `nikd10x` | Human | Factory, G0 merge, watch |
| `adh-dev-backend` | GitHub App | Cursor coder on backend repos |
| `adh-dev-frontend` | GitHub App | Cursor coder on frontend repos |
| `adh-dev-pm` | GitHub App | Hermes when a file must be committed on meta |
| `adh-reviewer` | GitHub App | Hermes reviewer; no merge |

## Merge policy

1. Black-box verify green.
2. `rubric-eng` overall ≥ **X = 2.7 / 3**. `process_integrity = 0` is a hard fail.
3. No blocker comments.
4. G0: Lead (`nikd10x`) clicks merge. Hermes cannot edit X.

PM artifacts use `rubric-pm` at PRD/Readout gates. Never one rubric for both lanes.

## Buzz (hard requirement)

Every orchestrator action and every long-running job broadcasts on Buzz: start, progress ≤90s, stall, done. Humans watch the room. No side channel.

## Harness feedback

Hermes proposes skill / `.mdc` / stack-constitution patches on Buzz (optional draft PR). Humans bake in. Agents never silently patch skills or push a stack repo.

## Proof tenant

Forked RealWorld (FastAPI + React), overlay harness only. Product PRs on `realworld-*`. Harness-issue PRs on `adh` / `adh-meta`.

## G0 kill tests

1. `adh-dev-backend` opens a PR on `realworld-api` only.
2. Same process cannot push `realworld-web`.
3. Identity cannot merge.
4. Checkpoint stop is honored.
5. Every step of that run is visible on Buzz (including verify).

## Out of scope for this stub

Wave-by-wave WorkManifest (`work/INIT-ADH-000.yaml`) is written after G0 kill tests pass and the first product INIT slice is chosen.
