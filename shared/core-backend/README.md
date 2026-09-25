Cross-slice backend modules built together in week 1:
- `auth/`      OTP login, JWT, roles (customer, worker, agency owner, admin)
- `dispatch/`  nearest-available-worker assignment, fallback by rating, booking status transitions
- `tracking/`  Socket.IO gateway for live worker location
Slices call these modules; they do not reimplement them.
