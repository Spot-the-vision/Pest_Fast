# Contributing

## Golden rules
1. Work inside your own slice. Touching another slice or `shared/` means a separate small PR.
2. Merge small and often. Open a PR at least once a day. Never save up a big merge for the end.
3. Never push to `main`. Every change goes through a PR with one teammate review and green CI.
4. Update your branch from `main` before opening the PR (`git pull --rebase origin main`).
5. Contract first. Change `shared/contracts/` in its own PR, merge it, then build against it.

## Branch names
`feat/<slice>/<short-task>`, `fix/<slice>/<short-bug>`, `chore/<area>/<short-task>`
Examples: `feat/worker/kyc-upload`, `feat/customer/slot-picker`, `chore/shared/ci`.

## Commits
Short and specific: `worker: add availability toggle endpoint`.

## Migrations (most common cause of crashes)
- File name: `YYYYMMDDHHMM__<slice>__<what>.sql`, e.g. `202609251030__worker__create_workers.sql`.
- Each table has exactly one owner slice. Other slices never alter it; they ask the owner or go through a service.
- Never edit a migration that is already merged. Add a new one.
- Prefer safe changes: add columns as nullable first, backfill, then tighten in a later migration.
- Every PR that touches migrations must pass "migrate from an empty database" in CI.

## Dependencies
- Add packages in a small PR of their own, so `package-lock.json` conflicts stay tiny.
- If the lockfile conflicts, take `main`'s version, rerun install, commit.

## Definition of done
- Typecheck, lint and tests pass in CI.
- Works on a real Android phone (frontend tasks) or through the API with a test (backend tasks).
- No secrets in the code. Sandbox keys only.
- A teammate reviewed it.

## Branch protection to enable on `main`
Require a pull request, require 1 approval, require code-owner review, require status checks (CI) to pass, require branches to be up to date before merging, block force pushes.
