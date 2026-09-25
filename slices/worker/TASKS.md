# Worker slice tasks

## Frontend
- [ ] Wire `slices/worker/frontend` into `apps/partner-app`
- [ ] Sign up and OTP login (uses shared auth)
- [ ] KYC form and document upload (no raw Aadhaar stored)
- [ ] Agency reference ID entry and validation
- [ ] Pending-approval screen
- [ ] Online/offline toggle
- [ ] Background location streaming (expo-location + expo-task-manager)
- [ ] Job offer screen: accept/reject with timeout
- [ ] Navigate to customer and mark arrived
- [ ] Complete job (notes, photos)
- [ ] Earnings screen

## Backend
- [ ] Worker profile and document endpoints
- [ ] Availability endpoint
- [ ] Location ingest endpoint (rate limited)
- [ ] Job accept/reject/arrived/complete endpoints (status changes go through dispatch)
- [ ] Earnings endpoint

## Migrations
- [ ] workers, worker_documents, worker_availability, worker_locations, worker_earnings

## Tests
- [ ] Endpoint tests for each backend task
- [ ] Manual test on a real Android phone: location works with the screen locked
