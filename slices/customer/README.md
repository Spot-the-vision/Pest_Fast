# Customer slice (Person 2)

Scope: customer signup, addresses, booking, payment, live tracking, history, ratings.
App shell: `apps/customer-app`.

Tables owned: `customers`, `addresses`, `bookings`, `payments`, `ratings`
Endpoints owned: `/customers/*`, `/bookings/*`, `/payments/*`, `/ratings/*`
Rule: booking status changes after creation happen only through `shared/core-backend/dispatch`.
Depends on: `shared/core-backend/auth`, `dispatch`, `tracking`
