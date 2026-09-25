# Rules for AI coding agents

Read this file before changing anything.

- Stack: React Native with Expo (customer + partner apps), NestJS + TypeScript (API), PostgreSQL + PostGIS, Redis, Socket.IO, React + Vite (admin web). Use the latest stable Expo SDK, and check the current docs before using any Expo or React Native API.
- Stay inside the slice you were assigned (`slices/<name>/`). Do not edit other slices or `shared/` unless the task says so.
- Code against `shared/contracts/`. Never invent request/response shapes.
- Never edit a merged migration. Add a new one using the naming rule in CONTRIBUTING.md.
- Never put secrets, API keys, real Aadhaar/PAN/bank data or production credentials in code, tests or fixtures. Use sandbox keys and fake data.
- Never store raw Aadhaar numbers.
- Do not add dependencies without saying why in the PR description.
- Do not merge or push to `main`. Open a PR.
- Every change needs a test or a clear manual test note in the PR.
- Say plainly what you did not finish or could not verify.
