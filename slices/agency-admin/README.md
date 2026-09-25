# Agency and admin slice (Person 3)

Scope: agency setup, worker approval and management, live map, bookings dashboard, services and pricing, complaints, reports.
App shell: `apps/admin-web`.

Tables owned: `agencies`, `agency_members`, `services`, `service_prices`, `complaints`
Endpoints owned: `/agencies/*`, `/admin/*`, `/services/*`
Depends on: `shared/core-backend/auth`, `tracking`; reads from worker and customer slices only through their services or API.
