# Worker slice (Person 1)

Scope: worker onboarding and KYC, availability, receiving and doing jobs, location streaming, earnings.
App shell: `apps/partner-app`.

Tables owned: `workers`, `worker_documents`, `worker_availability`, `worker_locations`, `worker_earnings`
Endpoints owned: `/workers/*`, `/worker-jobs/*`
Depends on: `shared/core-backend/auth`, `dispatch`, `tracking`
