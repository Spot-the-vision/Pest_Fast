# Customer slice tasks

## Frontend
- [ ] Wire `slices/customer/frontend` into `apps/customer-app`
- [ ] Sign up and OTP login (uses shared auth)
- [ ] Address add/select (map pin)
- [ ] Service and pest-type selection
- [ ] Slot picker
- [ ] Booking summary and confirm
- [ ] UPI payment flow (sandbox)
- [ ] Dispatch status screen (finding worker)
- [ ] Live tracking map with ETA
- [ ] Booking history and details
- [ ] Rating after job
- [ ] Cancel booking and support entry

## Backend
- [ ] Customer and address endpoints
- [ ] Create/cancel booking endpoints
- [ ] Payment order creation and webhook verification (server confirms payment)
- [ ] Ratings endpoint
- [ ] Booking history endpoint

## Migrations
- [ ] customers, addresses, bookings, payments, ratings

## Tests
- [ ] Endpoint tests for each backend task
- [ ] Manual test of the full booking flow on a real Android phone
